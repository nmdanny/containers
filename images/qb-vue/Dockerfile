FROM docker.io/library/alpine:3.21 AS builder

WORKDIR /app
RUN wget https://github.com/VueTorrent/VueTorrent/releases/download/v2.33.0/vuetorrent.zip && unzip vuetorrent.zip && rm vuetorrent.zip

FROM  ghcr.io/home-operations/qbittorrent:5.2.0@sha256:08eb7ed4c7fe70425064d58154c35fccc89fafffd64ce9d1affed399e173ff20
COPY --from=builder --chown=nobody:nogroup /app/vuetorrent /webui

