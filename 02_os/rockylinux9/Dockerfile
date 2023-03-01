## For SSH

FROM rockylinux:9

RUN yum -y install openssh-server

RUN sed -ri 's/^#PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config


RUN echo 'root:rootpass' | chpasswd

RUN ssh-keygen -t rsa -N "" -f /etc/ssh/ssh_host_rsa_key

EXPOSE 22

# start sshd
CMD ["/usr/sbin/sshd", "-D"]