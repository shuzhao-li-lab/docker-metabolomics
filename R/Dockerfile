# Copyright (c) 

# Distributed under the terms of the Modified BSD License.
ARG BASE_CONTAINER=jupyter/datascience-notebook
FROM $BASE_CONTAINER

LABEL maintainer="us"
LABEL tags="Metabolomics"

# Fix DL4006
SHELL ["/bin/bash", "-o", "pipefail", "-c"]

USER root

# BiocManager,     r-cran-biocmanager ?
# NetCDF Installation
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    netcdf-bin \
    libnetcdf-dev \
    && \
    rm -rf /var/lib/apt/lists/*

# Install mummichog 
RUN pip install \
    'networkx==1.10' \
    'xlsxwriter' \
    'mummichog==2.*' 

USER $NB_UID

# + from Jasmine https://github.com/xia-lab/MetaboAnalyst_Docker/blob/master/Dockerfile
# Install all R packages from Bioconductor 
RUN R -e 'install.packages("BiocManager", repos = "http://cran.us.r-project.org")'

RUN R -e 'BiocManager::install(version="3.10"); BiocManager::install(c("impute", "pcaMethods", "siggenes", "globaltest", "GlobalAncova", "Rgraphviz", "KEGGgraph", "preprocessCore", "genefilter", "SSPA", "sva", "limma", "mzID", "xcms"))' \
    && \
    fix-permissions "/home/${NB_USER}"


WORKDIR $HOME
