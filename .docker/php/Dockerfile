FROM php:8.0.5-fpm-alpine
ENTRYPOINT ["docker-php-entrypoint"]
WORKDIR /var/www/html
EXPOSE 9000

# Install and enable common php extensions
RUN apk add --no-cache zlib-dev libpng-dev libxml2-dev oniguruma-dev libcurl-dev curl-dev libzip-dev
RUN docker-php-ext-install gd xml mbstring curl ctype fileinfo zip json

# Install composer
RUN php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
RUN php composer-setup.php --install-dir=/usr/local/bin --filename=composer

CMD ["php-fpm"]