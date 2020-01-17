FROM php:7.2.9-alpine@sha256:b7470c2adc0163b91a27d0fd1e107b5fb57bacc28c682acd2514e8289e8fa50b

RUN apk add --no-cache zlib-dev=1.2.11-r1 \
    libmcrypt-dev=2.5.8-r7 \
    icu-libs=60.2-r2 \
    curl-dev=7.61.1-r2 \
    libmemcached-dev=1.0.18-r2 \
    gnupg=2.2.8-r0 \
    fontconfig=2.12.6-r1 \
    autoconf=2.69-r2 \
    $PHPIZE_DEPS

RUN pecl install memcached-3.0.4 \
    redis-4.1.1 \
    mongodb-1.4.4 \
    mcrypt-1.0.1

RUN docker-php-ext-enable memcached redis mongodb mcrypt

RUN docker-php-ext-configure intl
RUN docker-php-ext-install curl bcmath zip intl
