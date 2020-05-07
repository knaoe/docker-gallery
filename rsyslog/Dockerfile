FROM alpine:3.11

RUN apk --no-cache update \
    && apk add --no-cache \
      rsyslog=8.1911.0-r1 \
      rsyslog-mmfields=8.1911.0-r1

COPY rsyslog.conf /etc/rsyslog.conf

VOLUME /var/log
WORKDIR /var/log

ENV TZ=UTC

EXPOSE 514/tcp \
  514/udp

ENTRYPOINT ["rsyslogd", "-n"]