#Download base image centos
FROM  b3vis/prometheus_bot

WORKDIR /config
# Install influxdb
COPY config.yaml  /config

#CMD ["/usr/bin/influxd", "-config", "/etc/influxdb/influxdb.conf"]
CMD /go/bin/prometheus_bot -c /config/config.yaml

EXPOSE 9087
