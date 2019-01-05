FROM jenkins/jenkins
MAINTAINER Joaquin Jachura Chavez 0.3
USER root
RUN curl "https://bootstrap.pypa.io/get-pip.py" -o "get-pip.py" && python get-pip.py
RUN pip install awscli
RUN apt-get update && apt-get install -y vim net-tools sudo
RUN echo "StrictHostKeyChecking no" >> /etc/ssh/ssh_config
RUN echo 'jenkins ALL=(ALL) NOPASSWD:ALL' >> /etc/sudoers
RUN echo '%sudo ALL=(ALL:ALL) NOPASSWD:ALL' >> /etc/sudoers
USER jenkins
