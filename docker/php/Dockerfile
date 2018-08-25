FROM php:7.1-fpm

# Install recommended extensions for Symfony
RUN apt-get update && apt-get install -y \
        libicu-dev \
    && docker-php-ext-install \
        intl \
        opcache \
    && docker-php-ext-enable \
        intl \
        opcache \
    && docker-php-ext-install pdo pdo_mysql \
    && docker-php-ext-install mysqli

# Permission fix
RUN usermod -u 1000 www-data
