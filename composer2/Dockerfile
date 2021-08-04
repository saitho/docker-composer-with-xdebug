FROM php:7.2-fpm-alpine AS php72
COPY --from=composer/composer:2.1.5 /usr/bin/composer /usr/bin/composer
RUN apk add --no-cache --update alpine-sdk autoconf automake libtool gcc && pecl install xdebug-2.9.8 && docker-php-ext-enable xdebug

FROM php:7.4-fpm-alpine AS php74
COPY --from=composer/composer:2.1.5 /usr/bin/composer /usr/bin/composer
RUN apk add --no-cache --update alpine-sdk autoconf automake libtool gcc && pecl install xdebug-2.9.8 && docker-php-ext-enable xdebug
