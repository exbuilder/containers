ARG BASE_CONTAINER=rocker/verse:4.0.4
FROM $BASE_CONTAINER

LABEL maintainer="Katie Schuler <kathryn.schuler@gmail.com>"

# as root user
USER root

# get postgres prereqs
RUN apt-get update && \
    apt-get install -y libpq-dev && \
    apt-get clean && rm -rf /var/lib/apt/lists/*

# includes some R and python packages with the build
RUN install2.r --error \
    --deps TRUE \   
    infotheo \
    lme4 \
    RpostgreSQL \
    getpass \
    gridextra \
    stringdist 
