FROM php:8.2-fpm-alpine
ENTRYPOINT ["docker-php-entrypoint"]
WORKDIR /var/www/html
EXPOSE 9000

# Install and enable common php extensions
RUN apk add --no-cache bash nano zlib-dev libpng-dev libxml2-dev oniguruma-dev curl-dev libzip-dev
RUN docker-php-ext-install gd xml mbstring curl ctype fileinfo zip

# Install composer
RUN php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
RUN php composer-setup.php --install-dir=/usr/local/bin --filename=composer

CMD ["php-fpm"]