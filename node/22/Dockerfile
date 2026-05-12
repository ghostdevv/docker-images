FROM        node:22-trixie-slim

LABEL       author="Willow (GHOST)"
LABEL       maintainer="hello@willow.sh"
LABEL       org.opencontainers.image.source="https://github.com/ghostdevv/docker-images"

RUN         apt update -y
RUN         apt -y install ffmpeg iproute2 sqlite3 libsqlite3-dev python3 python3-dev ca-certificates dnsutils tzdata zip tar curl build-essential libtool git

RUN         npm -g install npm@10 # workaround as npm broke itself
RUN         npm -g install npm@11
RUN         npm -g install pnpm@10
RUN         npm -g install tsm@2

WORKDIR     /app

CMD         ["node"]
