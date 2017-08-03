FROM php:7.0-apache
RUN apt-get update && apt-get install -y\
	git \
    npm \
    wget

RUN docker-php-ext-install mysqli
RUN git clone https://github.com/WordPress/WordPress.git /var/www/html/
COPY config/php.ini /usr/local/etc/php/

EXPOSE 80
EXPOSE 443