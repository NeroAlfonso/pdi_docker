FROM debian:9
RUN apt-get update
RUN apt-get install libwebkitgtk-1.0-0 -y
RUN apt-get install default-jre -y
RUN apt-get install unzip -y
RUN apt-get install libaio1 -y
WORKDIR /usr/local
ENV JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64 \
    OPT=-Doracle.jdbc.timezoneAsRegion=false
ENV JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64
CMD ["/bin/sh", "/usr/local/pdi/9.1/data-integration/spoon.sh"]
