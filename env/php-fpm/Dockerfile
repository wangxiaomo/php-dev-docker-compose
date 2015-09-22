FROM php:5.6-fpm

#RUN apt-get update
#RUN apt-get install -y libpng12-dev libjpeg-dev
#RUN docker-php-ext-configure gd --with-png-dir=/usr --with-jpeg-dir=/usr
#RUN docker-php-ext-install gd

#RUN docker-php-ext-install mbstring
#RUN docker-php-ext-install gettext
#RUN docker-php-ext-install zip
RUN docker-php-ext-install mysqli

RUN echo "date.timezone = Asia/Shanghai" > /usr/local/etc/php/php.ini

COPY redis-2.2.7.tgz /home/redis.tgz
RUN pecl install /home/redis.tgz && echo "extension=redis.so" > /usr/local/etc/php/conf.d/redis.ini

ADD composer.phar /usr/local/bin/composer
RUN chmod 755 /usr/local/bin/composer
