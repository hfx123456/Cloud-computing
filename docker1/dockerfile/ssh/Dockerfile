#生成的新镜像以centos镜像为基础
FROM centos:7
MAINTAINER hfx
#升级系统
RUN yum -y update
#安装openssh-server
RUN yum -y install openssh-server
#修改/etc/ssh/sshd_config
RUN sed -i 's/UsePAM yes/UsePAM no/g' /etc/ssh/sshd_config
#将密钥文件复制到/etc/ssh/目录中
ADD ssh_host_rsa_key /etc/ssh/ssh_host_rsa_key
ADD ssh_host_rsa_key.pub /etc/ssh/ssh_host_rsa_key.pub
RUN mkdir -p /root/.ssh
ADD authorized_keys /root/.ssh/authorized_keys
RUN chown :ssh_keys /etc/ssh/ssh_host_rsa_key
RUN chown :ssh_keys /etc/ssh/ssh_host_rsa_key.pub
#将ssh服务启动脚本复制到/usr/local/sbin目录中，并改变权限为755
ADD run.sh /usr/local/sbin/run.sh
RUN chmod 755 /usr/local/sbin/run.sh
RUN echo "root:123456"|chpasswd
#开放窗口的22端口
EXPOSE 22
#运行脚本，启动sshd服务
CMD ["/usr/local/sbin/run.sh"]
