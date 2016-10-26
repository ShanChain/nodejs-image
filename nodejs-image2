#Version:0.0.1
FROM ubuntu:14.04
MAINTAINER snow "xuefeng.zhao@shanchain.com"
RUN rm /bin/sh && ln -s /bin/bash /bin/sh
RUN apt-get update && \
	apt-get install -y wget xz-utils 
RUN cd /opt && \
	wget https://nodejs.org/dist/v4.4.7/node-v4.4.7-linux-x64.tar.xz && \
	xz -d node-v4.4.7-linux-x64.tar.xz && \ 
	tar -xvf node-v4.4.7-linux-x64.tar && \
	rm -f node-v4.4.7-linux-x64.tar 
RUN ln -s /opt/node-v4.4.7-linux-x64/bin/node /usr/local/sbin/node
RUN ln -s /opt/node-v4.4.7-linux-x64/bin/npm /usr/local/sbin/npm
RUN npm install npm@3 -g
EXPOSE 80