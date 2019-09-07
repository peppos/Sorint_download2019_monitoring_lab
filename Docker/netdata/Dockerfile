#Download base image centos
FROM centos:latest

WORKDIR /opt

RUN yum install epel-release -y
RUN yum install stress httpd vim -y

COPY server-status.conf /etc/httpd/conf.d

RUN httpd

RUN chmod 755 /var/log/httpd
COPY index.html /var/www/html

# Install netdata
RUN curl -Ss https://my-netdata.io/kickstart.sh > kickstart.sh
RUN chmod 755 kickstart.sh
RUN ./kickstart.sh  --dont-wait 

COPY entrypoint.sh entrypoint.sh

CMD sh entrypoint.sh

EXPOSE 19999 80

