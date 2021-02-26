FROM ruby:2.7

ARG WORKDIR=/var/www/my-app

ENV LANG=C.UTF-8 TZ=Asia/Tokyo

RUN apt-get update && apt-get install -y nodejs npm mariadb-client

RUN gem install rails

RUN npm install -g yarn@1

RUN mkdir -p $WORKDIR

WORKDIR $WORKDIR

EXPOSE 3000
