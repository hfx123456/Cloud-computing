FROM  apache_dockerfile:centos
MAINTAINER hfx
#安装httpd
RUN yum install -y httpd &&yum clean all
#安装php
RUN yum install epel-release yum-utils -y
RUN yum install http://rpms.remirepo.net/enterprise/remi-release-7.rpm  -y
RUN yum-config-manager --enable remi-php72 -y
RUN yum install php php-mysql -y
VOLUME /var/www/html
EXPOSE 80

