FROM circleci/ruby:2.4.2-node
MAINTAINER Anshul <anshul@anshul.io>

USER root

RUN apt-get update -qq
RUN apt-get install -y -qq postgresql-client cmake
ENV DOCKERIZE_VERSION v0.6.0
RUN wget https://github.com/jwilder/dockerize/releases/download/$DOCKERIZE_VERSION/dockerize-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
    && tar -C /usr/local/bin -xzvf dockerize-linux-amd64-$DOCKERIZE_VERSION.tar.gz \
    && rm dockerize-linux-amd64-$DOCKERIZE_VERSION.tar.gz

USER circleci