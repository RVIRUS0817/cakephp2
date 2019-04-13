FROM php:7.2-fpm-alpine3.9
RUN curl -sS https://getcomposer.org/installer | php && \
    php composer.phar require "cakephp/cakephp":"~2.10" && \
    php -r "unlink('composer-setup.php');" && \
    mv composer.phar /usr/local/bin/composer && \
    apt-get update && \
    apt-get install -y libicu-dev && \
    docker-php-ext-install intl pdo_mysql mbstring && \
    apt-get install -y git && \
    apt-get install -y zip unzip && \
    composer config -g repos.packagist composer https://packagist.jp && \
    composer global require hirak/prestissimo