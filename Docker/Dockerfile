FROM rocker/r-ver:latest

LABEL maintainer="mhuang233@wisc.edu"

RUN apt-get update && apt-get install -y \
    libcurl4-openssl-dev \
    libssl-dev \
    libxml2-dev \
    libgit2-dev

RUN /rocker_scripts/install_tidyverse.sh

# RUN R -e "install.packages(c('devtools', 'tidyverse'), dependencies=TRUE)"

RUN R -e "install.packages('rstan', dependencies=TRUE)"

RUN R -e "remotes::install_github(repo = 'skdeshpande91/VCBART', subdir = 'VCBART')" > std0.out 2> std0.out

RUN R -e "remotes::install_github(repo = 'skdeshpande91/flexBART', subdir = 'flexBART')" > std1.out 2> std1.out


