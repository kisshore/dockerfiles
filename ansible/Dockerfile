FROM ubuntu:16.04
RUN apt-get update -y
RUN apt-get install software-properties-common -y
RUN apt-add-repository ppa:ansible/ansible
RUN apt-get update -y
RUN apt-get install ansible -y
RUN apt-get install openssh-server -y
RUN apt-get install vim -y
RUN mkdir /var/run/sshd
RUN echo 'root:screencast' | chpasswd
RUN sed -i 's/PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config
CMD ["/usr/sbin/sshd", "-D"]
EXPOSE 22
