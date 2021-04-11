ARG BASE_CONTAINER=rocker/verse:4.0.3
FROM $BASE_CONTAINER

LABEL maintainer="Katie Schuler <kathryn.schuler@gmail.com>"

# as root user
USER root

# get postgres prereqs
RUN apt-get update && \
    apt-get install -y libpq-dev && \
    apt-get clean && rm -rf /var/lib/apt/lists/* 

# change repo back to cran
RUN echo "options(repos = c(CRAN = 'https://cran.rstudio.com/'), download.file.method = 'libcurl')" >> /usr/local/lib/R/etc/Rprofile.site

# install more packages that we like to have
RUN install2.r --error \
    infotheo \
    lme4 \
    RPostgreSQL \
    getPass \
    gridExtra \
    tidyjson
