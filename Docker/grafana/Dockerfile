#Download base image centos
FROM centos:latest

COPY grafana.repo /etc/yum.repos.d/
COPY grafana-server /root
RUN chmod 755 /root/grafana-server

# Install grafana
RUN yum install grafana freetype* -y

CMD ["/root/grafana-server", "start"]
EXPOSE 3000
