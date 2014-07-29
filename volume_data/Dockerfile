FROM ubuntu:12.04


RUN apt-get update

RUN apt-get install -y vim wget git openssh-server

RUN mkdir /var/run/sshd

RUN echo 'root:root' |chpasswd

VOLUME ["/opt/config","/data"]

WORKDIR /data

CMD ["/usr/sbin/sshd","-D"]

EXPOSE 22