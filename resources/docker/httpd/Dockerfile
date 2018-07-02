FROM fpfis/httpd-php-dev:7.1

# Uploadprogress
RUN git clone https://github.com/php/pecl-php-uploadprogress/ /usr/src/php/ext/uploadprogress/ && \
    docker-php-ext-configure uploadprogress && \
    docker-php-ext-install uploadprogress && \
    rm -rf  /usr/src/php/ext/uploadprogress

RUN apk add --no-cache $( scanelf --needed --nobanner --format '%n#p' --recursive /usr/local | tr ',' '\n' | sort -u | awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' );