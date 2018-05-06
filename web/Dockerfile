FROM php:7-fpm-alpine

RUN mkdir /code
WORKDIR /code

RUN docker-php-ext-install pdo_mysql

RUN	chown -R www-data:www-data /code

RUN sed -ri 's/^www-data:x:82:82:/www-data:x:1000:50:/' /etc/passwd
