FROM fpfis/httpd-php-dev:7.1

# Uploadprogress
RUN git clone https://github.com/php/pecl-php-uploadprogress/ /usr/src/php/ext/uploadprogress/ && \
    docker-php-ext-configure uploadprogress && \
    docker-php-ext-install uploadprogress && \
    rm -rf  /usr/src/php/ext/uploadprogress

RUN apk add --no-cache patch