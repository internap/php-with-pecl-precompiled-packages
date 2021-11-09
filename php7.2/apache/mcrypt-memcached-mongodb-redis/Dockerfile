FROM php:7.2.34-apache@sha256:765365bf1dba8c46bdc198860d9fc183861c309049823d4174d32f9707b037d8

RUN apt-get update -q && DEBIAN_FRONTEND=noninteractive apt install -y libmcrypt-dev=2.5.8-3.3 \
    libcurl4-gnutls-dev=7.52.1-* \
    zlib1g-dev=1:1.2.8.* \
    libmemcached-dev=1.0.18-4.1 \
    gnupg2=2.1.18-8* \
    fontconfig=2.11.0-* \
  && rm -rf /var/lib/apt/lists/*

RUN pecl install memcached-3.0.4 \
    redis-4.1.1 \
    mongodb-1.4.4 \
    mcrypt-1.0.1

RUN docker-php-ext-enable memcached redis mongodb mcrypt

RUN docker-php-ext-install curl bcmath zip
