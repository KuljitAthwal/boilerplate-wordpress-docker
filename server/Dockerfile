FROM php:7.4.16-apache
RUN apt-get update 
RUN apt-get -y install git

RUN apt-get -y install wget

RUN docker-php-ext-install mysqli
RUN git clone https://github.com/WordPress/WordPress.git /var/www/html/
COPY config/php.ini /usr/local/etc/php/

EXPOSE 80
EXPOSE 443
