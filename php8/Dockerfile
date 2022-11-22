FROM php:8.1.11-apache

RUN echo "ServerName localhost" >> /etc/apache2/apache2.conf

COPY ./vhosts.conf /etc/apache2/sites-enabled/000-default.conf

CMD tail -f /dev/null

WORKDIR /var/www/