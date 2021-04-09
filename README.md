# exbuilder's docker images

This repository holds exbuilder's docker images. exbuilder takes a slow appraoch to building docker images for now: new images are only built when someone wants or needs one. If you want us to build a new container (e.g. with a particular R or Python version), you can request one by creating an issue or making a pull request.

## exbuilder/nginx

exbuilder's nginx image is an expansion of the [nginx](https://hub.docker.com/_/nginx) stable alpine image. It adds a user 'exbuilder' with necessary permissions and the configuration files required for nginx to serve your web experiments. 

## exbuilder/php

exbuilder's php image is an expansion of the [php](https://hub.docker.com/_/php) fpm alpine image. It adds a user `exbuilder` with necessary permissions and the drivers and configuration files required for working with exbuilder's postgres database. It also adds composer, which exbuilder needs to run the php scripts that write data to S3 buckets. 

## exbuilder/rstudio

exbuilder's RStudio image is an expansion of the [rocker/verse](https://hub.docker.com/r/rocker/verse) container. It adds a library for working with exbuilder's postgres database and the following r packages:  infotheo, lme4, RpostgreSQL, getPass, gridExtra. 

## exbuilder/jupyter

exbuilder's jupyter image is an expansion of the [jupyter/datascience-notebook](https://hub.docker.com/r/jupyter/datascience-notebook) container. It adds a library for working with exbuilder's postgres database and the following r packages: infotheo, lme4, RpostgreSQL, getPass, gridExtra, stringdist

### cite

You can cite exbuilder like this

```
    @misc{schuler2021exbuilder,
    author={Kathryn Schuler},
    title={Exbuilder: a framework for reproducible research with docker containers},
    year={2021},
    howpublished={available from https://github.com/exbuilder/exbuilder/}
    }
```