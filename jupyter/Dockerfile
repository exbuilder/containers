
ARG BASE_CONTAINER=jupyter/datascience-notebook:r-4.0.3
FROM $BASE_CONTAINER

LABEL maintainer="Katie Schuler <kathryn.schuler@gmail.com>"


USER root

# get postgres prereqs
RUN apt-get update && \
    apt-get install -y libpq-dev && \
    apt-get clean && rm -rf /var/lib/apt/lists/*

USER $NB_UID 

# includes some R and python packages with the build
RUN conda install --quiet --yes \
    'r-infotheo=1.2.0' \
    'r-lme4=1.1*' \
    'r-stringdist=0.9.6' \
    'r-getpass=0.2*' \
    'r-rpostgresql=0.6*'  \
    'r-gridextra=2.3*' && \
    conda clean --all -f -y && \
    fix-permissions "${CONDA_DIR}" && \
    fix-permissions "/home/${NB_USER}"
