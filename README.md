
# Metabolomics Docker Images

This is to try to compile a deck of Dockerfiles for tools in metabolomics.

The tools should be useful in real world applications, and the images should be as slim as possible.

## Python centric

Need Scipy deck. 

Working on mummichog. 

- pushed Debian busteer, Python 3.8.6 and mummichog 2.4.4.

Interested and suggesting: ..

- suggestions? 

## R centric

XCMS and related


## Java centric

MzMine 2, Biotransformer

## C++ centric

OpenMS


## based on the Jupyter Notebook Data Science Stack

- [jupyter/datascience-notebook](http://jupyter-docker-stacks.readthedocs.io/en/latest/using/selecting.html#jupyter-datascience-notebook)


## Sizes of a few images 

(on local disk, not compressed as on Docker Hub)

    shuzhao@P500:~$ docker images
    REPOSITORY                                           TAG                 IMAGE ID            CREATED             SIZE
    xcms-sl                                              latest              02a6ef231bc7        15 hours ago        1.32GB
    jasenfinch/ubuntu-r-xcms                             latest              e58f6dcef717        35 hours ago        1.69GB
    shuzhao/mummichog                                    2.4.4               9b0ac8067b4a        5 days ago          397MB
    yufree/xcms                                          latest              75d7c5534c58        8 days ago          4.66GB
    jupyter/datascience-notebook                         latest              49673ef00cad        2 weeks ago         3.87GB
    jupyter/r-notebook                                   latest              9039544f4be3        2 weeks ago         2.6GB
    ubuntu                                               18.04               56def654ec22        4 weeks ago         63.2MB
    jupyter/scipy-notebook                               latest              75d7f5e4f76d        3 months ago        3.99GB
    chambm/pwiz-skyline-i-agree-to-the-vendor-licenses   latest              cd8991c6aabb        5 months ago        3.99GB
    continuumio/miniconda3                               latest              b4adc22212f1        7 months ago        429MB
    hello-world                                          latest              bf756fb1ae65        9 months ago        13.3kB
    r-base                                               3.5.3               62c848eeb175        19 months ago       649MB
    rocker/r-ver                                         3.5                 afdb7a43ba17        19 months ago       605MB


