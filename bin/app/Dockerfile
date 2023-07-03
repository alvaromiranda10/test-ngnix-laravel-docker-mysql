FROM php:8.2-fpm

RUN apt update && \
    apt install --no-install-recommends -y \
    git \
    zlib1g-dev \
    libpng-dev \
    libzip-dev \
    unzip

RUN docker-php-ext-install \
    pdo_mysql \
    zip

COPY --from=composer /usr/bin/composer /usr/bin/composer