FROM php:7.4-fpm-alpine AS php74
COPY --from=composer/composer:1.10.22 /usr/bin/composer /usr/bin/composer
RUN apk add --no-cache --update alpine-sdk autoconf automake libtool gcc && pecl install xdebug-2.9.8 && docker-php-ext-enable xdebug
