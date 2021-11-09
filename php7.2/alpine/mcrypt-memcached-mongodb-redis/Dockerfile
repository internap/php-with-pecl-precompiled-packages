FROM php:7.2.34-alpine3.12@sha256:4361c0c2767145d7fce396bd0a677dc716a4173e28c27ccf27cd345bd388c839

RUN apk add --no-cache zlib-dev=1.2.11-r3 \
    libmcrypt-dev=2.5.8-r8 \
    curl-dev=7.79.1-r0 \
    libmemcached-dev=1.0.18-r4 \
    gnupg=2.2.23-r1 \
    fontconfig=2.13.1-r2 \
    autoconf=2.69-r2 \
    $PHPIZE_DEPS

RUN pecl install memcached-3.0.4 \
    redis-4.1.1 \
    mongodb-1.4.4 \
    mcrypt-1.0.1

RUN docker-php-ext-enable memcached redis mongodb mcrypt

RUN docker-php-ext-install curl bcmath zip
