FROM php:7-fpm-alpine

WORKDIR /var/www/html
ADD ./panel /var/www/html

RUN docker-php-ext-install pdo_mysql

RUN	chown -R www-data:www-data /var/www/html

RUN sed -ri 's/^www-data:x:82:82:/www-data:x:1000:50:/' /etc/passwd
