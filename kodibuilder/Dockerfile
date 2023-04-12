FROM debian:bookworm

RUN echo "deb-src http://deb.debian.org/debian bookworm main" >> /etc/apt/sources.list

RUN apt-get update \
  && apt-get -y -u build-dep kodi \
  && apt-get -y -u -V install \
    git \
    libbz2-dev \
    libgles2-mesa-dev \
    libglm-dev \
    libmodplug-dev \
    libpcap-dev \
    libprojectm-dev \
    libwavpack-dev \
    libxi-dev \
    lsb-release