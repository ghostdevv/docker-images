FROM        node:20-bookworm-slim

LABEL       author="Willow (GHOST)"
LABEL       maintainer="ghostdevbusiness@gmail.com"
LABEL       org.opencontainers.image.source="https://github.com/ghostdevv/docker-images"

RUN         apt update -y
RUN         apt -y install ffmpeg iproute2 sqlite3 libsqlite3-dev python3 python3-dev ca-certificates dnsutils tzdata zip tar curl build-essential libtool git

RUN         npm -g install npm@10
RUN         npm -g install pnpm@8
RUN         npm -g install tsm

RUN         useradd -m -d /home/container container
USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

CMD         ["node"]
