FROM php:5.5.33-fpm
RUN apt-get clean
RUN apt-get update
RUN apt-get install -y \
        libzip-dev \
	        zip \
		  && docker-php-ext-configure zip --with-libzip \
		    && docker-php-ext-install zip
RUN docker-php-ext-install mysqli
RUN addgroup www-data www-data
RUN rm -rf /var/www/*
RUN mkdir /var/www/novinano
RUN chown www-data:www-data /var/www/novinano/
USER www-data
