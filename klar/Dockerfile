FROM alpine:3.10.3

LABEL MAINTAINER "hari.karthigasu@gmail.com"

ARG KLAR_VERSION="2.4.0"

ADD https://github.com/optiopay/klar/releases/download/v${KLAR_VERSION}/klar-${KLAR_VERSION}-linux-amd64 klar

RUN chmod +x klar \
    && mv klar /usr/local/bin

ENTRYPOINT ["/bin/sh"]
