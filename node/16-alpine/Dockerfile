FROM        node:16-alpine

LABEL       author="Willow (GHOST)"
LABEL       maintainer="ghostdevbusiness@gmail.com"
LABEL       org.opencontainers.image.source="https://github.com/ghostdevv/docker-images"

RUN         apk update
RUN         apk add git python3

RUN         npm -g install npm@9
RUN         npm -g install pnpm@8
RUN         npm -g install tsm

WORKDIR     /container

CMD         ["node"]
