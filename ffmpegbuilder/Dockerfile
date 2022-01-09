FROM debian:bullseye

RUN echo "deb-src http://deb.debian.org/debian bullseye main" >> /etc/apt/sources.list

RUN apt-get update \
  && apt-get -y build-dep ffmpeg \
  && apt-get install -y -u -V clang curl git libsmbclient-dev tree wget
