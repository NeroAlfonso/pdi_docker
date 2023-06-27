#docker build --no-cache -t pentahojava:1.0.0 . --network=host
FROM debian:10
RUN apt-get update
RUN apt-get install gnupg -y
RUN apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 3B4FE6ACC0B21F32
RUN echo "deb http://cz.archive.ubuntu.com/ubuntu bionic main universe" >> /etc/apt/sources.list
RUN apt-get update
RUN apt-get install libwebkitgtk-1.0-0 -y
#RUN apt-get install default-jre -y
RUN apt-get install openjdk-8-jdk -y
WORKDIR /usr/local
ENV JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64 \
OPT=-Doracle.jdbc.timezoneAsRegion=false
ENV JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64
#RUN apt-get install libwebkitgtk-1.0-0 -y
#RUN apt-get install default-jre -y
#WORKDIR /usr/local
#ENV JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64 \
#    OPT=-Doracle.jdbc.timezoneAsRegion=false
#ENV JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64

