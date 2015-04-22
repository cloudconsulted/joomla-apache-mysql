FROM ubuntu

MAINTAINER Olivier Beaudet <obeaudet@hotmail.com>

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y mysql-server apache2 git php5 php5-imap php5-mcrypt php5-gd php5-curl php5-mysql php-pear

RUN chown -R www-data:www-data /var/www

EXPOSE 80
