FROM docker.io/centos 

MAINTAINER Su 


WORKDIR /usr

RUN mkdir jdk

ADD  jdk1.8.0_231 jdk

ENV JAVA_HOME=/usr/jdk
ENV JRE_HOME=$JAVA_HOME/jre
ENV CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar:$JRE_HOME/lib:$CLASSPATH
ENV PATH=/sbin:$JAVA_HOME/bin:$PATH

WORKDIR /root

RUN mkdir webapps 

ADD webapp webapps

#RUN curl http://repo.mysql.com/mysql-community-release-el7-5.noarch.rpm
#RUN rpm -ivh /root/mysql-community-release-el7-5.noarch.rpm
RUN yum install -y mysql-server
#RUN systemctl start mysqld 
#RUN systemctl enable mysqld

EXPOSE 8080
EXPOSE 3306
EXPOSE 80
EXPOSE 443

CMD java -jar /root/webapps/forum-1.0-SNAPSHOT.jar
#CMD systemctl start mysqld.service
