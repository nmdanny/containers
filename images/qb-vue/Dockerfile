FROM docker.io/library/alpine:3.21 AS builder

WORKDIR /app
RUN wget https://github.com/VueTorrent/VueTorrent/releases/download/v2.23.1/vuetorrent.zip && unzip vuetorrent.zip && rm vuetorrent.zip

FROM ghcr.io/onedr0p/qbittorrent:5.0.4
COPY --from=builder --chown=nobody:nogroup /app/vuetorrent /webui

