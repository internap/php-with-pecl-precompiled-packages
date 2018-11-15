# php with PECL precompiled package

This repostory allows to store pre-built php images with PECL embedded.
Reinstalling PECL packages everytime is a slow process and we want to benefit
from docker cache as much as possible.

## Variants
For now the project provides images for -alpine and -apache variant of the official
 php library. it's based on 7.2 because it's currently the best practice.

[https://hub.docker.com/_/php/](https://hub.docker.com/_/php/)

php7.2-alpine-mcrypt-memcached-mongodb-redis:1.0

php7.2-apache-mcrypt-memcached-mongodb-redis:1.0



## Image size

This was taken experimetally

| VARIANT | SIZE   |
| ------- | -------|
| apache  | ~440MB |
| alpine  | ~318MB |
