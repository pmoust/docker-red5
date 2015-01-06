FROM java:8
MAINTAINER Panagiotis Moustafellos <pmoust@gmail.com>

ENV DEBIAN_FRONTEND noninteractive
ENV RED5_RELEASE 1.0.2

RUN apt-get update && \
    apt-get install -y wget && \
    apt-get clean && \
    wget -q https://github.com/Red5/red5-server/releases/download/v${RED5_RELEASE}-RELEASE/red5-server-${RED5_RELEASE}-RELEASE-server.tar.gz && \
    tar -xzf red5-server-${RED5_RELEASE}-RELEASE-server.tar.gz && \
    mv red5-server-${RED5_RELEASE}-RELEASE /opt/red5 && \
    rm red5-server-${RED5_RELEASE}-RELEASE-server.tar.gz

VOLUME ["/opt/red5"]

EXPOSE 843 1935 5080 5443 8088 8443 9999

WORKDIR /opt/red5

ENTRYPOINT ["./red5.sh"]
