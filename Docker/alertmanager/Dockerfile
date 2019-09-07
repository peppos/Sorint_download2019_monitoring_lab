#Download base image centos
FROM centos:latest

WORKDIR /opt/alertmanager

# Install prometeus
RUN curl -L 'https://github.com/prometheus/alertmanager/releases/download/v0.17.0/alertmanager-0.17.0.linux-amd64.tar.gz' -o /tmp/alertmanager.tar.gz
RUN tar -xf /tmp/alertmanager.tar.gz -C /opt/alertmanager/ --strip-components 1

CMD ["/opt/alertmanager/alertmanager"]
EXPOSE 9093
