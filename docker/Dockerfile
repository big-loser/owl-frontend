FROM centos:latest

RUN yum install -y wget xz
RUN wget -P /tmp/ https://nodejs.org/dist/v11.13.0/node-v11.13.0-linux-x64.tar.xz 
RUN unxz /tmp/node-v11.13.0-linux-x64.tar.xz
RUN tar -xvf /tmp/node-v11.13.0-linux-x64.tar
RUN mv /tmp/node-v11.13.0-linux-x64 /opt/nodejs  

ENV PATH /opt/nodejs/bin:$PATH

ADD nodejs-test /opt/

ENTRYPOINT npm run dev
