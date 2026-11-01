FROM php:8.4-fpm

WORKDIR "/application"

RUN apt-get update && apt-get install -y \
    curl \
    zip \
    unzip \
    nano \
    libzip-dev \
    libicu-dev \
    && docker-php-ext-configure intl \
    && docker-php-ext-install intl zip pdo_mysql \
    && curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer \
    && apt-get clean && rm -rf /var/lib/apt/lists/*