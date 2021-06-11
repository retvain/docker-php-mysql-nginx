FROM php:8.0-fpm-alpine

COPY ./conf /usr/local/etc/php/conf.d
RUN chmod -R 664 /usr/local/etc/php/conf.d

RUN docker-php-ext-install pdo_mysql mysqli && apk add autoconf && apk add gcc && apk update && apk add --no-cache curl git npm

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

WORKDIR /var/www

EXPOSE 9000
