FROM ubuntu:16.04
#Docker File for Jenkins Installation on Ubuntu
RUN export https_proxy=https://10.24.252.50:80 &&\
    export http_proxy=http://10.24.252.50:80 &&\
    apt-get update &&\
    apt-get install -y wget
RUN export https_proxy=https://10.24.252.50:80 &&\
    export http_proxy=http://10.24.252.50:80 &&\ 
	wget -q -O - https://jenkins-ci.org/debian/jenkins-ci.org.key | apt-key add - &&\
	sh -c 'echo deb http://pkg.jenkins-ci.org/debian binary/ > /etc/apt/sources.list.d/jenkins.list' &&\
	apt-get update &&\
	apt-get install -y default-jre &&\
	apt-get install -y default-jdk
COPY ./scripts/jenkins.war /
RUN chmod +x /jenkins.war
CMD [ "sh", "-c", "nohup java -jar jenkins.war > log.txt; bash"]
EXPOSE 8080

