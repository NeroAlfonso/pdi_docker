FROM debian:9
RUN apt-get update
RUN apt-get install libwebkitgtk-1.0-0 -y
RUN apt-get install default-jre -y
WORKDIR /usr/local
ENV JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64 \
    OPT=-Doracle.jdbc.timezoneAsRegion=false
ENV JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64
CMD ["/bin/sh", "/usr/local/pdi/spoon.sh"]
