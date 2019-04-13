FROM php:7.2.10-fpm-stretch
RUN apt-get update && \
    apt-get install -y curl git zip unzip libicu-dev && \ 
    curl -sS https://getcomposer.org/installer | php && \
    php composer.phar require "cakephp/cakephp":"~2.10" && \
    php -r "unlink('composer-setup.php');" && \
    mv composer.phar /usr/local/bin/composer && \
    docker-php-ext-install intl pdo_mysql mbstring && \
    composer config -g repos.packagist composer https://packagist.jp && \
    composer global require hirak/prestissimo