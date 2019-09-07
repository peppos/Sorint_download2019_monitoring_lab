#Download base image centos
FROM centos:latest

WORKDIR /opt

RUN yum install epel-release -y


# Install netdata
RUN curl -Ss https://my-netdata.io/kickstart.sh > kickstart.sh
RUN chmod 755 kickstart.sh
RUN ./kickstart.sh  --dont-wait 

CMD ["netdata", "-D"]

EXPOSE 19999

