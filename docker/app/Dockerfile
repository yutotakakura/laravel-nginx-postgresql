FROM php:8.2-fpm

COPY ./docker/app/php.ini /usr/local/etc/php/php.ini

COPY --from=composer /usr/bin/composer /usr/bin/composer

RUN apt-get update && \
    apt-get -y install \
    git \
    zip \
    unzip \
    libpq-dev \
    && docker-php-ext-install pdo_pgsql bcmath \ 
    && pecl install xdebug \
    && docker-php-ext-enable xdebug

WORKDIR /var/www/html