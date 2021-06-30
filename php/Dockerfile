FROM php:7.4-fpm-alpine

# RUN docker-php-ext-install pdo_mysql zlib gd ldap zip imap
ADD https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/

RUN chmod +x /usr/local/bin/install-php-extensions && sync && \
    install-php-extensions gd pdo_mysql zlib ldap zip imap

CMD ["php-fpm"]

EXPOSE 9000
