ARG RELEASE
FROM debian:${RELEASE}

RUN dpkg --add-architecture arm64 && apt-get update && \
	apt-get install -y bc bison build-essential cpio debhelper \
	device-tree-compiler dosfstools flex gcc-aarch64-linux-gnu \
	gcc-arm-none-eabi git jq kmod libelf-dev libfdt-dev libgnutls28-dev \
	libpython3-dev libssl-dev libssl-dev:arm64 lzop mtools parted python3 \
	python3-pyelftools python3-setuptools rsync sudo swig zstd
