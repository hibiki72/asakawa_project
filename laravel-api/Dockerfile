FROM php:8.1-fpm

RUN apt-get update && apt-get install -y libpng-dev zip libzip-dev libonig-dev

RUN docker-php-ext-install pdo pdo_mysql mbstring gd zip exif pcntl

WORKDIR /var/www

COPY . /var/www

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN composer install
