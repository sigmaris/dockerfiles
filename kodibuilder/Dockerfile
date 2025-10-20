ARG RELEASE
FROM debian:$RELEASE
ARG RELEASE

RUN echo "deb-src http://deb.debian.org/debian $RELEASE main" >> /etc/apt/sources.list

RUN apt-get update \
	&& apt-get -y -u build-dep kodi \
	&& apt-get -y -u -V install \
	git \
	libbz2-dev \
	libflac-dev \
	libgles2-mesa-dev \
	libglm-dev \
	libjsoncpp-dev \
	libmodplug-dev \
	libmpeg2-4-dev \
	libmpg123-dev \
	libpcap-dev \
	libprojectm-dev \
	libtinyxml2-dev \
	libturbojpeg0-dev \
	libusb-1.0-0-dev \
	libwavpack-dev \
	libxi-dev \
	lsb-release \
	ninja-build \
	sudo
