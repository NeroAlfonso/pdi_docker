FROM debian:9
RUN apt-get update
RUN apt-get install libwebkitgtk-1.0-0 -y
RUN apt-get install default-jre -y
RUN apt-get install curl -y
WORKDIR /usr/local
ENV JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64 \
    OPT=-Doracle.jdbc.timezoneAsRegion=false
ENV JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64
ENV SUPERCRONIC_URL=https://github.com/aptible/supercronic/releases/download/v0.1.12/supercronic-linux-amd64 \
    SUPERCRONIC=supercronic-linux-amd64 \
    SUPERCRONIC_SHA1SUM=048b95b48b708983effb2e5c935a1ef8483d9e3e
RUN curl -fsSLO "$SUPERCRONIC_URL" \
 && echo "${SUPERCRONIC_SHA1SUM}  ${SUPERCRONIC}" | sha1sum -c - \
 && chmod +x "$SUPERCRONIC" \
 && mv "$SUPERCRONIC" "/usr/local/bin/${SUPERCRONIC}" \
 && ln -s "/usr/local/bin/${SUPERCRONIC}" /usr/local/bin/supercronic
COPY scripts /usr/local/scripts
COPY crontab /etc/crontabs/crontab
ENTRYPOINT ["supercronic"]
CMD ["/etc/crontabs/crontab"]
