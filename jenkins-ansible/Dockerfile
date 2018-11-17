FROM jenkins/jenkins
MAINTAINER Joaquin Jachura Chavez 0.2
USER root
RUN curl "https://bootstrap.pypa.io/get-pip.py" -o "get-pip.py" && python get-pip.py
RUN pip install -U ansible 
RUN apt-get update && apt-get install -y vim net-tools
RUN sed 's/#   StrictHostKeyChecking ask/StrictHostKeyChecking no/g' /etc/ssh/ssh_config
USER jenkins
