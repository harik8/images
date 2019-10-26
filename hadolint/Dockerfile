FROM alpine:3.10.3

LABEL MAINTAINER "hari.karthigasu@gmail.com"

ARG HADOLINT_VERSION="1.17.2"
ARG CURL_VERSION=7.66.0

ADD https://github.com/hadolint/hadolint/releases/download/v${HADOLINT_VERSION}/hadolint-Linux-x86_64 hadolint

RUN apk update \
    && apk add curl=${CURL_VERSION} --no-cache \
    && chmod +x hadolint \
    && mv hadolint /usr/local/bin

ENTRYPOINT ["hadolint"]
