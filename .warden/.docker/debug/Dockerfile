ARG WARDEN_IMAGE_REPOSITORY
ARG PHP_VERSION
ARG XDEBUG_VERSION

FROM ${WARDEN_IMAGE_REPOSITORY}/php-fpm:${PHP_VERSION}-${XDEBUG_VERSION:-debug}

RUN sudo dnf install -y postgresql php-pgsql \
    && dnf clean all \
    && sudo rm -rf /var/cache/dnf

USER www-data