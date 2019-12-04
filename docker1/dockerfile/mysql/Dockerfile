FROM test:v4

MAINTAINER Sh
RUN yum install mariadb-server mariadb -y
RUN systemctl start mariadb
RUN systemctl enable mariadb.service
EXPOSE  80
