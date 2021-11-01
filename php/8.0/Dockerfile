FROM php:8.0-fpm-alpine

WORKDIR /var/www/html

RUN apk --update add &&\
    apk add libzip-dev &&\
    docker-php-ext-install mysqli pdo pdo_mysql zip

# Installing composer
RUN curl -sS https://getcomposer.org/installer -o composer-setup.php
RUN php composer-setup.php --install-dir=/usr/local/bin --filename=composer
RUN rm -rf composer-setup.php

RUN apk add nodejs npm

EXPOSE 9000