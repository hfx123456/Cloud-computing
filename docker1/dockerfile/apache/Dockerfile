From  5588/centos-ssh:v1.0.0
MAINTAINER  hfx
#创建者的基本信息

#设置环境变量，所有操作都是非交互式的
ENV DEBIAN_FRONTEND noninteractive

#安装
RUN yum install httpd -y

ADD run.sh /run.sh
RUN chmod 755 /*.sh
EXPOSE 80
WORKDIR /app
CMD ["/run.sh"]
