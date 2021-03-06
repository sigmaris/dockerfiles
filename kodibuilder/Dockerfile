ARG CODENAME

FROM debian:$CODENAME

ARG CODENAME

RUN apt-get update && apt-get install -y apt-transport-https gnupg ca-certificates

COPY rockpkgs.key /

RUN apt-key add /rockpkgs.key

RUN echo "deb https://sigmaris.github.io/rockpkgs $CODENAME main" > /etc/apt/sources.list.d/sigmarisrockpkgs.list

RUN if [ "$CODENAME" = "buster" ]; then echo "deb http://deb.debian.org/debian buster-backports main" > /etc/apt/sources.list.d/backports.list ; fi

RUN apt-get update && apt-get install -y -u -V \
	autoconf \
	automake \
	autopoint \
	build-essential \
	cmake \
	debhelper \
	default-jre \
	default-libmysqlclient-dev \
	dh-python \
	doxygen \
	fontforge-nox \
	fonts-dejavu-core \
	fonts-droid-fallback \
	gawk \
	gettext \
	git \
	gperf \
	groovy \
	libarchive-dev \
	libasound2-dev \
	libass-dev \
	libavahi-client-dev \
	libavahi-common-dev \
	libavahi-core-dev \
	libavahi-compat-libdnssd-dev \
	libavcodec-dev \
	libavfilter-dev \
	libavformat-dev \
	libavutil-dev \
	libbluetooth-dev \
	libbluray-dev \
	libbz2-dev \
	libcap-dev \
	libcdio-dev \
	libcec-dev \
	libde265-dev \
	libcommons-lang-java \
	libcrossguid-dev \
	libcurl4-gnutls-dev \
	libcwiid-dev \
	libdav1d-dev \
	libdbus-1-dev \
	libdrm-dev \
	libegl1-mesa-dev \
	libenca-dev \
	libflac-dev \
	$([ "$CODENAME" = "bullseye" ] && echo libflatbuffers-dev) \
	libfluidsynth-dev \
	libfmt-dev \
	libfontconfig-dev \
	libfreetype6-dev \
	libfribidi-dev \
	libfstrcmp-dev \
	libgbm-dev \
	libgcrypt-dev \
	libgif-dev \
	libgles2-mesa-dev \
	libglew-dev \
	libglm-dev \
	libglu1-mesa-dev \
	libgnutls28-dev \
	libgpg-error-dev \
	libgtest-dev \
	libhdhomerun-dev \
	libheif-dev \
	libinput-dev \
	libiso9660-dev \
	libjpeg-dev \
	libjsoncpp-dev \
	liblcms2-dev \
	liblirc-dev \
	libltdl-dev \
	liblz4-dev \
	liblzma-dev \
	liblzo2-dev \
	libmagickcore-dev \
	libmagickwand-6-headers \
	libmagickwand-dev \
	libmicrohttpd-dev \
	libmodplug-dev \
	libmp3lame-dev \
	libnfs-dev \
	libogg-dev \
	libopenmpt-dev \
	libp8-platform-dev \
	libpcap-dev \
	libpcre3-dev \
	libplist-dev \
	libpng-dev \
	libpostproc-dev \
	libprojectm-dev \
	libpugixml-dev \
	libpulse-dev \
	librapidxml-dev \
	libraw-dev \
	libresid-builder-dev \
	librsvg2-bin \
	librtmp-dev \
	libshairplay-dev \
	libsidplay2-dev \
	libsidutils-dev \
	libsmbclient-dev \
	libspdlog-dev \
	libsqlite3-dev \
	libswresample-dev \
	libswscale-dev \
	libssh-dev \
	libssl-dev \
	libtag1-dev \
	libtiff-dev \
	libtinyxml-dev \
	libtinyxml2-dev \
	libtool \
	libturbojpeg0-dev \
	libudev-dev \
	libudfread-dev \
	libunistring-dev \
	libusb-1.0-0-dev \
	libva-dev \
	libvdpau-dev \
	libvorbis-dev \
	libxkbcommon-dev \
	libxrandr-dev \
	libxslt1-dev \
	libxt-dev \
	libz3-dev \
	linux-libc-dev \
	lsb-release \
	meson \
	nlohmann-json3-dev \
	$([ "$CODENAME" = "bullseye" ] && echo opengl-image-dev) \
	pkg-config \
	$([ "$CODENAME" = "buster" ] && echo python-dev) \
	python3-dev \
	rapidjson-dev \
	swig \
	unzip \
	uuid-dev \
	yasm \
	zip \
	zlib1g-dev
