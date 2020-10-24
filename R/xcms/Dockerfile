FROM rocker/r-ver:3.5


# NetCDF Installation
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    netcdf-bin \
    libnetcdf-dev \
    libhdf5-dev \
    libxml2-dev \
    && \
    rm -rf /var/lib/apt/lists/*


RUN Rscript -e \
  'install.packages(c("BiocManager","devtools","tidyverse","RcppEigen")); \
  BiocManager::install("xcms")'
