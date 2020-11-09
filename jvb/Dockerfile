ARG JITSI_REPO=goodic
FROM ${JITSI_REPO}/base-java

RUN \
	apt-dpkg-wrap apt-get update && \
	apt-dpkg-wrap apt-get install -y jitsi-videobridge2 jq curl iproute2 jq && \
	apt-cleanup

COPY rootfs/ /

COPY scripts /scripts/

RUN /fix-permissions.sh

VOLUME /config

USER 1001
