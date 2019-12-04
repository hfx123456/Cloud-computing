FROM test:v2
MAINTAINER  hfx
RUN yum install rsync -y
COPY latest.tar.gz /app
RUN  tar xzvf latest.tar.gz
RUN rsync -avP /app/wordpress/ /var/www/html/
RUN mkdir /var/www/html/wp-content/uploads
RUN chown -R apache:apache /var/www/html/*
#暴露端口
EXPOSE  80                                                                                                                                          
                                                                                                                                                                                                                                                                           
                                                                                                                                           
                                                                                                                                           
                                                                                                                                           
                                                                                                                                           

