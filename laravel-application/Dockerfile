FROM php:8.4-fpm

RUN mv "$PHP_INI_DIR/php.ini-production" "$PHP_INI_DIR/php.ini"

COPY --from=composer:2.8.8 /usr/bin/composer /usr/bin/composer

RUN curl -sL https://deb.nodesource.com/setup_23.x | bash \
   && apt-get install -y nodejs

COPY --chown=www-data:www-data . /var/www/html

RUN composer install --no-dev --no-interaction
RUN npm install

RUN php artisan optimize
