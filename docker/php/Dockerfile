FROM php:8.0-fpm

# enable symfony-cli
RUN echo 'deb [trusted=yes] https://repo.symfony.com/apt/ /' | tee /etc/apt/sources.list.d/symfony-cli.list

RUN apt-get update && apt-get install -y git libzip-dev zip unzip wget symfony-cli
RUN docker-php-ext-install zip

RUN wget https://getcomposer.org/download/latest-stable/composer.phar \
    && mv composer.phar /usr/local/bin/composer && chmod +x /usr/local/bin/composer

