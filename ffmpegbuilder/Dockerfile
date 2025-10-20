ARG RELEASE
FROM debian:${RELEASE}
ARG RELEASE

RUN sed -i -e 's/^Types: deb$/Types: deb deb-src/g' /etc/apt/sources.list.d/debian.sources

RUN apt-get update \
	&& apt-get -y build-dep ffmpeg \
	&& apt-get install -y -u -V clang curl git libsmbclient-dev sudo tree wget
