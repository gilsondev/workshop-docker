FROM ubuntu:latest
MAINTAINER Gilson Filho <me@gilsondev.in>

ENV MYSQL_MAJOR 5.7

RUN apt-get update

RUN apt-get install -y mysql-server

ADD custom.conf /var/lib/mysql
