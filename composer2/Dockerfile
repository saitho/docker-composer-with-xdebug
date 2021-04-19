FROM composer:2.0.8

RUN apk add --no-cache --update alpine-sdk autoconf automake libtool gcc && pecl install xdebug-2.9.8 && docker-php-ext-enable xdebug
