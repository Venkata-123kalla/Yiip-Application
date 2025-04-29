FROM php:7.4-apache

RUN apt-get update && apt-get install -y \
    libpng-dev libjpeg-dev libfreetype6-dev zip git unzip \
    && docker-php-ext-configure gd \
    && docker-php-ext-install gd pdo pdo_mysql

COPY src /var/www/html
RUN chown -R www-data:www-data /var/www/html

EXPOSE 80
