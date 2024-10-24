FROM mcr.microsoft.com/devcontainers/php:1-8.2-bookworm

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get install -y libpq-dev \ 
    && apt-get clean -y && rm -rf /var/lib/apt/lists/*

RUN docker-php-ext-configure pgsql -with-pgsql=/usr/local/pgsql \
    && docker-php-ext-install pdo pdo_pgsql pgsql

# Open Telemetry
RUN pecl install opentelemetry \
    && docker-php-ext-enable opentelemetry
