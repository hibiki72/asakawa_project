FROM php:8.1-fpm

# PHPの拡張機能のインストール
RUN docker-php-ext-install pdo pdo_mysql

# Composerのインストール
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR /var/www

COPY . .

RUN composer install
