# Strip down version of Dockerfile used for building and running the actual application
FROM php:8.2-fpm-alpine

RUN apk add --no-cache nginx supervisor \
    curl \
    git \
    unzip \
    libpq-dev \
    $PHPIZE_DEPS \
    postgresql-client

RUN docker-php-ext-install pdo pdo_pgsql

RUN pecl install opentelemetry \
    && docker-php-ext-enable opentelemetry

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer