FROM ubuntu:16.04
#Docker File for Jenkins Installation on Ubuntu
RUN apt-get update &&\
    apt-get install -y wget
RUN apt-get update &&\
	apt-get install -y default-jre &&\
	apt-get install -y default-jdk
COPY ./scripts/jenkins.war /
RUN chmod +x /jenkins.war
CMD [ "sh", "-c", "nohup java -jar jenkins.war > log.txt; bash"]
EXPOSE 8080
