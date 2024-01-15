ARG WARDEN_IMAGE_REPOSITORY
ARG PHP_VERSION

FROM ${WARDEN_IMAGE_REPOSITORY}/php-fpm:${PHP_VERSION}

RUN sudo dnf install -y postgresql php-pgsql \
    && dnf clean all \
    && sudo rm -rf /var/cache/dnf

WORKDIR /var/www/html
USER www-data