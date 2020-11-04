ARG CODENAME

FROM debian:$CODENAME

ARG CODENAME

RUN echo "deb-src http://deb.debian.org/debian $CODENAME main" >> /etc/apt/sources.list

RUN apt-get update \
  && apt-get -y build-dep ffmpeg \
  && apt-get install -y -u -V curl git libdc1394-22-dev libsrt-gnutls-dev tree wget
