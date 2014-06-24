FROM ubuntu:14.04

MAINTAINER FAN FEI(feifan.pub@gmail.com)


RUN apt-get update
RUN apt-get upgrade -y

RUN apt-get install -y openssh-server supervisor vim lsof
RUN mkdir -p /var/run/sshd
RUN mkdir -p /var/log/supervisor

# root password for ssh service
RUN echo 'root:futureDial1' |chpasswd

# enable root login
RUN sed -i "s/^PermitRootLogin\s*without-password$/PermitRootLogin yes/g" /etc/ssh/sshd_config

ADD supervisord.conf /etc/supervisor/conf.d/supervisord.conf
ADD sshd.conf /etc/supervisor/conf.d/sshd.conf

EXPOSE 22

CMD ["/usr/bin/supervisord"]

