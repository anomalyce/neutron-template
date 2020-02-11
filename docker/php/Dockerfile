FROM php:7.3-fpm

RUN apt-get update --fix-missing && \
    apt-get install -y curl build-essential libxml2-dev libzip-dev zip libgmp-dev

RUN docker-php-ext-configure zip --with-libzip && \
    docker-php-ext-install pdo pdo_mysql mysqli bcmath ctype json mbstring xml zip gmp

RUN usermod -u 1000 www-data

