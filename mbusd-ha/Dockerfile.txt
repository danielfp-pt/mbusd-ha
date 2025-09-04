FROM alpine:latest
RUN apk add --no-cache mbusd bash
COPY mbusd.conf /etc/mbusd.conf
COPY run.sh /run.sh
RUN chmod +x /run.sh
CMD ["/run.sh"]
