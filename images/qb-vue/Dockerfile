FROM docker.io/library/alpine:3.21 AS builder

WORKDIR /app
RUN wget https://github.com/VueTorrent/VueTorrent/releases/download/v2.36.1/vuetorrent.zip && unzip vuetorrent.zip && rm vuetorrent.zip

FROM  ghcr.io/home-operations/qbittorrent:5.3.0@sha256:5a858e61f94cf2712391db32ed03556576c700858f3e62c4c6fcde262443ebd8
COPY --from=builder --chown=nobody:nogroup /app/vuetorrent /webui

