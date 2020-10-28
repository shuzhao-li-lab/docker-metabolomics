FROM rocker/r-ver:4.0.3

# NetCDF Installation
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    netcdf-bin \
    libnetcdf-dev \
    libhdf5-dev \
    libxml2-dev \
    libglpk-dev \
    && \
    rm -rf /var/lib/apt/lists/*


RUN Rscript -e \
  'install.packages(c("BiocManager","devtools","tidyverse","RcppEigen", "Hmisc")); \
  BiocManager::install(c("xcms", "CAMERA")); \
  devtools::install_github("cbroeckl/RAMClustR"); \
  devtools::install_github("yufree/mz.unity")'
  

ENTRYPOINT ["bin/bash"]
