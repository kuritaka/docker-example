FROM ubuntu:22.04

LABEL maintainter="taka"

RUN apt-get update && \
apt-get install -y --no-install-recommends openssh-server

RUN sed -i 's/#PermitRootLogin without-password/PermitRootLogin yes/' /etc/ssh/sshd_config
RUN sed -i 's/#Port 22/Port 20022/' /etc/ssh/sshd_config

COPY ./files/id_rsa.pub /root/.ssh/authorized_keys

COPY ./files/setup.sh /root/
RUN  chmod a+x /root/setup.sh
RUN  echo "/root/setup.sh" >> /root/.bashrc