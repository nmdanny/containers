FROM docker.io/library/alpine:3.21 AS builder

WORKDIR /app
RUN wget https://github.com/VueTorrent/VueTorrent/releases/download/v2.27.0/vuetorrent.zip && unzip vuetorrent.zip && rm vuetorrent.zip

FROM  ghcr.io/home-operations/qbittorrent:5.1.2@sha256:a724f86a39fa637fc4ff81165585d7273dc9dcd9ca59818a34e9fa9c467dd26c
COPY --from=builder --chown=nobody:nogroup /app/vuetorrent /webui

