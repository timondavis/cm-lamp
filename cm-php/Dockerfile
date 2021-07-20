FROM php:8.0.8-fpm
RUN pecl install redis-5.3.4 \
    && pecl install xdebug-3.0.4 \
    && docker-php-ext-enable redis xdebug
RUN docker-php-ext-install mysqli
RUN echo "xdebug.mode=debug" \
    >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
RUN echo "xdebug.start_with_session_request=yes" \
    >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
RUN echo "xdebug.client_host=host.docker.internal" \
    >> /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
