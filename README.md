# exbuilder's docker images

exbuilder takes a slow appraoch to building docker images. New containers are only built when someone wants or needs one. If you want us to build a new container, you can request one by creating an issue or making a pull request. 

## exbuilder/nginx

exbuilder's nginx image is an expansion of the [nginx]() stable alpine image. It adds a user 'exbuilder' with necessary permissions and the configures files required for nginx to serve your web experiments. 

## exbuilder/php

exbuilder's php image is an expansion of the [php]() fpm alpine image. It adds a user `exbuilder` with necessary permissions and the drivers and configuration files required for working with exbuilder's postgres database. It also adds composer, which exbuilder needs to run the php scripts that write data to S3 buckets. 

## exbuilder/rstudio

exbuilder's RStudio image is an expansion of the [rocker/verse]() container. It adds a library for working with exbuilder's postgres database and the following packages: 

## exbuilder/jupyterlab

exbuilder's Jupyter Lab image is an expansion of the [jupyter/datascience-notebook]() container. It adds a library for working with exbuilder's postgres database and the following packages: 

