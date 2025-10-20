ARG RELEASE
FROM debian:${RELEASE}
ARG RELEASE

RUN echo "deb-src http://deb.debian.org/debian $RELEASE main" >> /etc/apt/sources.list

RUN apt-get update \
	&& apt-get -y build-dep ffmpeg \
	&& apt-get install -y -u -V clang curl git libsmbclient-dev sudo tree wget
