FROM php:7-apache

LABEL maintainer="andrew.brown5717@gmail.com"

RUN apt-get update -y && apt-get upgrade -y && apt-get autoclean -y && apt-get autoremove -y
RUN apt-get install -y vim build-essential wget curl git zip unzip

ADD ./scripts/install_composer.sh /tmp

RUN touch ~/.bashrc && chmod 766 ~/.bashrc

ADD ./apache-config.conf /etc/apache2/sites-enabled/000-default.conf
ADD ./php.ini /usr/local/etc/php

#RUN docker-php-ext-install mbstring mcrypt pdo pdo_mysql

RUN bash /tmp/install_composer.sh

#WORKDIR /var/www/html

#CMD ["apache2-foreground"]
