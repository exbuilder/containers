# syntax=docker/dockerfile:experimental
FROM nginx:stable-alpine

ADD ./nginx.conf /etc/nginx/nginx.conf
ADD ./default.conf /etc/nginx/conf.d/default.conf

RUN mkdir -p /var/www/html

RUN addgroup -g 1000 exbuilder && adduser -G exbuilder -g exbuilder -s /bin/sh -D exbuilder

RUN chown exbuilder:exbuilder /var/www/html
