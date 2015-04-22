FROM ubuntu

MAINTAINER Olivier Beaudet <obeaudet@hotmail.com>

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y mysql-server apache2 git php5 php5-imap php5-mcrypt php5-gd php5-curl php5-mysql

RUN wget https://github.com/joomla/joomla-cms/releases/download/3.4.1/Joomla_3.4.1-Stable-Full_Package.tar.gz --directory-prefix=/tmp
RUN tar -zxvf Joomla_3.4.1-Stable-Full_Package.tar.gz wget
RUN rm -rf /var/www/html/*
RUN cp -r /tmp/www/* /var/www/html/

RUN chown -R www-data:www-data /var/www

EXPOSE 80
