FROM jenkins/jenkins
MAINTAINER Joaquin Jachura Chavez 0.2
USER root
RUN curl "https://bootstrap.pypa.io/get-pip.py" -o "get-pip.py" && python get-pip.py
RUN apt-get install net-tools vim -y &&  pip install -U ansible 
RUN sed 's/#   StrictHostKeyChecking ask/StrictHostKeyChecking no/g' /etc/ssh/ssh_config
USER jenkins
