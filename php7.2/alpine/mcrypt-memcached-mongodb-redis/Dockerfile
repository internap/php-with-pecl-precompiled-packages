FROM php:7.2.9-alpine3.7@sha256:2a5e38c14e669a1d2274bf1cba46c2926800e08c4bae34e4b1fa301f1bd449fd

RUN apk add --no-cache zlib-dev=1.2.11-r1 \
    libmcrypt-dev=2.5.8-r7 \
    curl-dev=7.61.1-r3 \
    libmemcached-dev=1.0.18-r2 \
    gnupg=2.2.3-r1 \
    fontconfig=2.12.6-r0 \
    autoconf=2.69-r2 \
    $PHPIZE_DEPS

RUN pecl install memcached-3.0.4 \
    redis-4.1.1 \
    mongodb-1.4.4 \
    mcrypt-1.0.1

RUN docker-php-ext-enable memcached redis mongodb mcrypt

RUN docker-php-ext-install curl bcmath zip
