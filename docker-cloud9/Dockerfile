# DOCKER-VERSION 0.6.4

FROM ubuntu:14.04

#RUN echo deb http://archive.ubuntu.com/ubuntu precise main universe multiverse > /etc/apt/sources.list
RUN apt-get update && \
	apt-get install -y software-properties-common && \
	add-apt-repository -y ppa:chris-lea/node.js && \
	apt-get update && \
	apt-get install -y nodejs git && \
	git clone https://github.com/ajaxorg/cloud9.git
RUN cd /cloud9 && npm install

VOLUME ["/workspace"]

EXPOSE 3131
CMD ["/cloud9/bin/cloud9.sh", "-l", "0.0.0.0", "-w", "/workspace"]
