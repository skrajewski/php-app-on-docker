FROM php:7.1-fpm

RUN apt-get update && apt-get install -y \
	libmcrypt-dev \
    zlib1g-dev \
    libicu-dev \
    g++

RUN docker-php-ext-configure intl
RUN docker-php-ext-install -j$(nproc) iconv mcrypt mysqli pdo_mysql mbstring intl
