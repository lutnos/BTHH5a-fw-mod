FROM ubuntu:16.04

MAINTAINER Dave English <dave@lutnos.com>

ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update
RUN apt-get install -qq \
  build-essential git u-boot-tools zlib1g-dev rsync curl squashfs-tools \
  lzma-alone vim fakeroot python

RUN mkdir -p /workdir/files
WORKDIR /workdir
COPY 0-vars .
COPY *.sh ./
RUN chmod +x *.sh
COPY files files/

EXPOSE 8000
