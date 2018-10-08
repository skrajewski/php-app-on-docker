FROM php:7.2-fpm

RUN apt-get update && apt-get install -y \
    libmcrypt-dev \
    zlib1g-dev \
    libicu-dev \
    g++

RUN docker-php-ext-install -j$(nproc) iconv mysqli pdo_mysql mbstring intl

RUN yes | pecl install xdebug-2.6.1 mcrypt-1.0.1 \
    && docker-php-ext-enable xdebug mcrypt
