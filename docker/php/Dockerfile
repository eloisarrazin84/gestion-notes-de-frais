FROM php:8.2-fpm

RUN apt-get update && apt-get install -y \
    git unzip libzip-dev libpng-dev libonig-dev \
    && docker-php-ext-install pdo_mysql zip gd

WORKDIR /var/www/html
COPY ./app /var/www/html
RUN chown -R www-data:www-data /var/www/html && chmod -R 755 /var/www/html
