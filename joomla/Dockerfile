FROM ubuntu

MAINTAINER Olivier Beaudet <obeaudet@hotmail.com>

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y mysql-server apache2 git php5 php5-imap php5-mcrypt php5-gd php5-curl php5-apcu php5-mysqlnd

ADD https://github.com/joomla/joomla-cms/releases/download/3.4.1/Joomla_3.4.1-Stable-Full_Package.tar.gz /tmp/joomla/
RUN tar -zxvf /tmp/joomla/Joomla_3.4.1-Stable-Full_Package.tar.gz -C /tmp/joomla/
RUN rm -rf /var/www/html/*
RUN cp -r /tmp/joomla/* /var/www/html/
RUN mv /var/www/html/htaccess.txt /var/www/html/.htaccess

RUN chown -R www-data:www-data /var/www

EXPOSE 80

# By default, simply start apache.
CMD /usr/sbin/apache2ctl -D FOREGROUND
