FROM fpfis/cloud9

RUN yum install -y git && yum clean all
ENV COMPOSER_VERSION 1.6.5
ENV COMPOSER_ALLOW_SUPERUSER 1
RUN curl -L https://github.com/composer/composer/releases/download/${COMPOSER_VERSION}/composer.phar > /usr/local/bin/composer
RUN chmod +x /usr/local/bin/composer
COPY ./bin/php /usr/bin/php
