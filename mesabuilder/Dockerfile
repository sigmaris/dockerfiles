FROM debian:buster

RUN echo "deb http://deb.debian.org/debian buster-backports main" >> /etc/apt/sources.list

RUN apt-get update && apt-get install -y apt-transport-https git gnupg ca-certificates

COPY rockpkgs.key /

RUN apt-key add /rockpkgs.key

RUN echo "deb https://sigmaris.github.io/rockpkgs buster main" > /etc/apt/sources.list.d/sigmarisrockpkgs.list

RUN apt-get update && apt-get install -y \
	build-essential \
	debhelper \
	glslang-tools \
	meson \
	quilt \
	pkg-config \
	libdrm-dev=2.4.99-1 \
	libx11-dev \
	libxxf86vm-dev \
	libexpat1-dev \
	libsensors-dev \
	libxfixes-dev \
	libxdamage-dev \
	libxext-dev \
	libva-dev \
	libvdpau-dev \
	libvulkan-dev \
	x11proto-dev \
	linux-libc-dev \
	libx11-xcb-dev \
	libxcb-dri2-0-dev \
	libxcb-glx0-dev \
	libxcb-xfixes0-dev \
	libxcb-dri3-dev \
	libxcb-present-dev \
	libxcb-randr0-dev \
	libxcb-sync-dev \
	libxrandr-dev \
	libxshmfence-dev \
	python3 \
	python3-mako \
	python3-setuptools \
	flex \
	bison \
	llvm-8-dev \
	libelf-dev \
	libwayland-dev \
	libwayland-egl-backend-dev \
	libclang-8-dev \
	libclc-dev=0.2.0+git20190306 \
	wayland-protocols \
	zlib1g-dev \
	libglvnd-core-dev

RUN git clone https://github.com/sigmaris/mesa.git
