FROM httpd:2.4
RUN apt-get update; \
    apt-get upgrade;

# Copy host files
COPY ./vhost.conf /usr/local/apache2/conf/vhost.conf

# Copy apache vhost file to proxy php requests to php-fpm container
RUN echo "Include /usr/local/apache2/conf/vhost.conf" \
    >> /usr/local/apache2/conf/httpd.conf
