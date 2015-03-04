FROM ubuntu:14.04
MAINTAINER Zhe Feng <zhe@jumiduo.com>

ENV MONGO_VERSION 2.6.8

RUN apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 7F0CEB10
RUN echo 'deb http://downloads-distro.mongodb.org/repo/ubuntu-upstart dist 10gen' | tee /etc/apt/sources.list.d/mongodb.list
RUN apt-get update
RUN apt-get install -y mongodb-org=$MONGO_VERSION mongodb-org-server=$MONGO_VERSION mongodb-org-shell=$MONGO_VERSION mongodb-org-mongos=$MONGO_VERSION mongodb-org-tools=$MONGO_VERSION

VOLUME ["/data/db"]

EXPOSE 27017
EXPOSE 28017

CMD ["mongod"]
