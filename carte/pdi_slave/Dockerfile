FROM debian:9
RUN apt-get update
RUN apt-get install libwebkitgtk-1.0-0 -y
RUN apt-get install default-jre -y
ENV JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64 \
    OPT=-Doracle.jdbc.timezoneAsRegion=false
ENV JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64
WORKDIR /usr/local
COPY slave_config slave_config
RUN chmod +x slave_config -R
CMD ["/bin/sh", "/usr/local/pdi/carte.sh", "/usr/local/slave_config/carte_config.xml"]
