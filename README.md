joomla-apache-mysql
==================

An updated image from the kuthz/docker repo. This is a very basic joomla! install to be used to test and demo Joomla builds.


Packaged
--------

    Base image ubuntu
    Apache
    Mysql
    PHP5
    Joomla 3.4.1

Installation
------------
docker pull cloudconsulted/joomla

Running this image
------------------
docker run -d -p 80:80 cloudconsulted/joomla

Point your browser to http://localhost to start the installation wizard.

Database information
user:root
pwd:(leave it blank)




