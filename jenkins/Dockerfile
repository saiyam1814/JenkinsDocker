from centos:7

MAINTAINER Saiyam Pathak<saiyam911@gmail.com>

RUN yum -y install java-1.8.0-openjdk.x86_64 wget sudo git ansible

RUN useradd jenkins

WORKDIR /home/jenkins

RUN echo "jenkins ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers

ENV JAVA_HOME="/usr/lib/jvm/jre-1.8.0-openjdk"

RUN wget http://mirrors.jenkins.io/war-stable/latest/jenkins.war

RUN wget https://download.docker.com/linux/static/stable/x86_64/docker-17.03.1-ce.tgz

RUN tar -xvf docker-17.03.1-ce.tgz

RUN  cp docker/* /usr/bin/

ENTRYPOINT ["/bin/bash","-c", "sudo java -jar jenkins.war"]
