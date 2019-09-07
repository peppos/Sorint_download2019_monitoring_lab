#Download base image centos
FROM centos:latest

# Install influxdb
COPY influxdb.repo /etc/yum.repos.d
RUN yum install influxdb -y

CMD ["/usr/bin/influxd", "-config", "/etc/influxdb/influxdb.conf"]
EXPOSE 8086 8088
