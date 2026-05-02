ARG RELEASE
FROM debian:$RELEASE
ARG RELEASE
ARG QAIRT_VERSION=2.42.0.251225

RUN sed -i -e 's/^Types: deb$/Types: deb deb-src/g' /etc/apt/sources.list.d/debian.sources

RUN apt-get update \
	&& apt-get -y -u build-dep gst-plugins-bad1.0 onnxruntime \
	&& apt-get -y -u -V install \
	curl \
	git \
	sudo \
	unzip

RUN curl -L -o "/tmp/qairt-${QAIRT_VERSION}.zip" "https://softwarecenter.qualcomm.com/api/download/software/sdks/Qualcomm_AI_Runtime_Community/All/${QAIRT_VERSION}/v${QAIRT_VERSION}.zip"
RUN unzip "/tmp/qairt-${QAIRT_VERSION}.zip" && mv "qairt/${QAIRT_VERSION}" /opt/qairt && rmdir qairt && rm "/tmp/qairt-${QAIRT_VERSION}.zip"
