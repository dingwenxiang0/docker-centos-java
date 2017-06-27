FROM centos:7

MAINTAINER Ding Wen Xiang "624380857@qq.com"

ARG JAVA_MINOR_VERSION=80

ENV JRE_HOME=/app/tools/java/jre
ENV PATH=$PATH:$JRE_HOME/bin
ENV CLASSPATH=.:$JRE_HOME/lib:$CLASSPATH

ADD https://raw.githubusercontent.com/dingwenxiang0/docker-centos-java/master/oracle_download_cookies /tmp/oracle_download_cookies

RUN yum -y update \
    && yum -y install wget \
	&& OHS_COOKIE=`cat /tmp/oracle_download_cookies` \
    && mkdir -p /app/tools/java \
    && cd /app/tools/java \
    && wget --no-check-certificate --no-cookies --header "Cookie: $OHS_COOKIE oraclelicense=accept-securebackup-cookie;" http://download.oracle.com/otn/java/jdk/7u$JAVA_MINOR_VERSION-b15/jre-7u$JAVA_MINOR_VERSION-linux-x64.tar.gz \
    && tar -zxf jre-7u$JAVA_MINOR_VERSION-linux-x64.tar.gz \
    && ln -s /app/tools/java/jre1.7.0_$JAVA_MINOR_VERSION /app/tools/java/jre \
    && yum -y remove wget \
    && yum clean all \
    && java -version \
    && rm -rf jre-7u$JAVA_MINOR_VERSION-linux-x64.tar.gz \
	&& rm -rf /tmp/oracle_download_cookies
    
CMD ["/bin/bash"]