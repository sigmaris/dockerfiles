FROM debian:bullseye

RUN apt-get update && apt-get install -y apt-transport-https gnupg ca-certificates

COPY rockpkgs.key /

RUN apt-key add /rockpkgs.key

RUN echo "deb https://sigmaris.github.io/rockpkgs bullseye main" > /etc/apt/sources.list.d/sigmarisrockpkgs.list
RUN echo "deb-src http://deb.debian.org/debian bullseye main" >> /etc/apt/sources.list

RUN apt-get update \
  && apt-get -y -u build-dep kodi \
  && apt-get -y -u -V install \
    git \
    lsb-release
