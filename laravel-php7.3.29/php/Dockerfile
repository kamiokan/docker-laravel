FROM php:7.3.29-apache
RUN apt-get update \
  && apt-get install -y zlib1g-dev \
  && apt-get install -y unzip \
  && apt-get install -y libzip-dev \
  && docker-php-ext-install pdo_mysql mysqli mbstring zip \
  && docker-php-ext-enable mysqli \
  && a2enmod rewrite

# composer install
RUN curl -sS https://getcomposer.org/installer | php \
  && mv composer.phar /usr/local/bin/composer \
  && chmod +x /usr/local/bin/composer

WORKDIR /var/www/html

ENV COMPOSER_ALLOW_SUPERUSER 1
ENV COMPOSER_HOME /composer
ENV PATH $PATH:/composer/vendor/bin
# timezone
ENV TZ=Asia/Tokyo

