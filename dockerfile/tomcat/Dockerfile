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

EXPOSE 8080
EXPOSE 443

CMD java -jar /root/webapps/forum-1.0-SNAPSHOT.jar
