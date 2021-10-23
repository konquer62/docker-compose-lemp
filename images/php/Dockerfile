FROM php:8.0.12-fpm-alpine3.13
RUN docker-php-ext-install mysqli
RUN addgroup www-data www-data
RUN chown www-data:www-data /var/www/html/
USER www-data
