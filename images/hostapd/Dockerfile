FROM docker.io/library/alpine:3.22

RUN apk add --update --no-cache hostapd wireless-regdb iw

USER 1000:1000

ENTRYPOINT ["hostapd"]
