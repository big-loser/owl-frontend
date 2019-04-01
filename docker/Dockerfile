FROM centos:latest

RUN yum install -y wget xz
RUN wget -P /opt/ https://nodejs.org/dist/v11.13.0/node-v11.13.0-linux-x64.tar.xz 
RUN unxz /opt/node-v11.13.0-linux-x64.tar.xz
RUN tar -xvf /opt/node-v11.13.0-linux-x64.tar
RUN ln -s /opt/node-v11.13.0-linux-x64 /opt/nodejs  

ENV PATH /opt/nodejs/bin:$PATH

ADD nodejs-test /opt/

ENTRYPOINT npm run dev
