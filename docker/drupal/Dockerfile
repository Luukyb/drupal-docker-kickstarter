FROM drupal:8

RUN apt-get update -qq \
  && apt-get install wget mysql-client -yq

RUN apt-get install vim -y

RUN usermod -u 1000 www-data

ADD vhost.conf /etc/apache2/sites-available/000-default.conf

RUN a2ensite 000-default

WORKDIR /var/www/web
