FROM docker.io/library/alpine:3.21 AS builder

WORKDIR /app
RUN wget https://github.com/VueTorrent/VueTorrent/releases/download/v2.31.0/vuetorrent.zip && unzip vuetorrent.zip && rm vuetorrent.zip

FROM  ghcr.io/home-operations/qbittorrent:5.1.4@sha256:25fc7caf22101f85276ede9b1f76a46b7a93971bb6b70b6c58d14d6ab7f51415
COPY --from=builder --chown=nobody:nogroup /app/vuetorrent /webui

