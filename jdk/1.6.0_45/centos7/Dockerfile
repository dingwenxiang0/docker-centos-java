FROM centos:7

MAINTAINER Ding Wen Xiang "624380857@qq.com"

ARG JAVA_MINOR_VERSION=45

ENV JAVA_HOME=/app/tools/java/jdk
ENV PATH=$PATH:$JAVA_HOME/bin:$JAVA_HOME/jre/bin
ENV CLASSPATH=.:$JAVA_HOME/lib:$JAVA_HOME/jre/lib:$CLASSPATH

ADD https://github.com/dingwenxiang0/docker-centos-java/blob/master/oracle_download_cookies /tmp/oracle_download_cookies

RUN yum -y update \
    && yum -y install wget \
	&& OHS_COOKIE=`cat /tmp/oracle_download_cookies` \
    && mkdir -p /app/tools/java \
    && cd /app/tools/java \
    && wget --no-check-certificate --no-cookies --header "Cookie: $OHS_COOKIE oraclelicense=accept-securebackup-cookie;" https://edelivery.oracle.com/akam/otn/java/jdk/6u$JAVA_MINOR_VERSION-b06/jdk-6u$JAVA_MINOR_VERSION-linux-x64.bin \
	&& chmod 744 jdk-6u$JAVA_MINOR_VERSION-linux-x64.bin \
	&& ./jdk-6u$JAVA_MINOR_VERSION-linux-x64.bin \
    && ln -s /app/tools/java/jdk1.6.0_$JAVA_MINOR_VERSION /app/tools/java/jdk \
    && yum -y remove wget \
    && yum clean all \
    && java -version \
    && rm -rf jdk-6u$JAVA_MINOR_VERSION-linux-x64.bin \
	&& rm -rf /tmp/oracle_download_cookies
    
CMD ["/bin/bash"]