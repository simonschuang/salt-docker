FROM debian:jessie
MAINTAINER simon.s.chuang@gmail.com

ENV VERSION 2016.11

RUN apt-get update && apt-get install -y wget
RUN wget -O - https://repo.saltstack.com/apt/debian/8/amd64/${VERSION}/SALTSTACK-GPG-KEY.pub | apt-key add -

RUN echo "deb http://repo.saltstack.com/apt/debian/8/amd64/${VERSION} jessie main" > /etc/apt/sources.list.d/saltstack.list
RUN apt-get update

RUN apt-get install -y salt-master

ADD entrypoint.sh /entrypoint.sh

ENTRYPOINT ["/entrypoint.sh"]
