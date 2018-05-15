FROM php:7-fpm-alpine

RUN mkdir /code
WORKDIR /code
VOLUME ./project /code

RUN apk update
RUN apk add curl && rm -rf /var/cache/apk/*
RUN curl --silent --show-error https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
RUN docker-php-ext-install pdo_mysql

RUN chown -R www-data:www-data /code

RUN sed -ri 's/^www-data:x:82:82:/www-data:x:1000:50:/' /etc/passwd
