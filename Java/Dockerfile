FROM openjdk:16-slim-buster

LABEL maintainer=shuzhao

# MzMine 2 and BioTransformerJar

# https://github.com/biorack/metatlas/tree/main/docker/mzmine
ENV MZMINE_VERSIONS /home/$NB_USER/work/mzmine_components/versions

RUN apt-get update && apt-get install -y --no-install-recommends wget unzip\
	&& rm -rf /var/lib/apt/lists/*

RUN mkdir -p $MZMINE_VERSIONS && \
    cd $MZMINE_VERSIONS && \
    wget https://github.com/mzmine/mzmine2/releases/download/v2.53/MZmine-2.53-Linux.zip && \
    unzip MZmine-2.53-Linux.zip && \
    rm MZmine-2.53-Linux.zip && \
    cd .. && \
    mkdir biotransformer && cd biotransformer && \
    wget https://bitbucket.org/djoumbou/biotransformerjar/src/master/biotransformer-1.1.5.jar


ENTRYPOINT ["bin/bash"]
