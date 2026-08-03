FROM php:8.5-fpm-alpine

COPY --from=ghcr.io/mlocati/php-extension-installer /usr/bin/install-php-extensions /usr/local/bin/

RUN install-php-extensions \
    bcmath \
    bz2 \
    calendar \
    exif \
    gd \
    intl \
    ldap \
    mbstring \
    mysqli \
    opcache \
    pdo_mysql \
    pdo_pgsql \
    pgsql \
    redis \
    soap \
    sockets \
    uuid \
    xsl \
    zip \
    mongodb \
    @composer \
    && rm /usr/local/bin/install-php-extensions

RUN mkdir -p /.composer && chmod -R 777 /.composer
