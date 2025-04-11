FROM php:8.4-fpm

WORKDIR /var/www/html

RUN apt-get update && apt-get install -y --no-install-recommends \
    zip unzip git libpq-dev libonig-dev libxml2-dev libcurl4-openssl-dev \
    libjpeg-dev libpng-dev libfreetype6-dev libzip-dev libicu-dev libxslt1-dev \
    && docker-php-ext-configure gd --with-freetype --with-jpeg \
    && docker-php-ext-install -j$(nproc) \
    pdo pdo_mysql mysqli mbstring exif pcntl bcmath intl gd xml zip opcache soap xsl \
    && pecl install xdebug redis \
    && docker-php-ext-enable xdebug redis \
    && apt-get clean && rm -rf /var/lib/apt/lists/*

COPY php.ini /usr/local/etc/php/php.ini

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer