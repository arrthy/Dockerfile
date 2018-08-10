FROM ubuntu:16.04
#Docker File for ssh Installation on Ubuntu
RUN apt-get update &&\
	apt-get install -y openssh-server
RUN mkdir /var/run/sshd
CMD [ "sh", "-c", "/usr/sbin/sshd -D; bash"]
EXPOSE 22
