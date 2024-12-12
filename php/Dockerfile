FROM php:8.2-fpm

ARG DEBIAN_MIRROR_DOMAIN
ARG PHP_EXTENSIONS

RUN sed -i "s|deb.debian.org|${DEBIAN_MIRROR_DOMAIN}|g" /etc/apt/sources.list.d/debian.sources

RUN export option="--no-install-recommends -y" \
    && apt-get $option update \
    && apt-get $option install tzdata curl \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*


RUN curl -sSLf -o /usr/local/bin/install-php-extensions https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions \
    && chmod +x /usr/local/bin/install-php-extensions \
    && install-php-extensions $PHP_EXTENSIONS

WORKDIR /www
