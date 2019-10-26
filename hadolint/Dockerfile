FROM alpine:3.10.3

MAINTAINER "hari.karthigasu@gmail.com"

ARG HADOLINT_VERSION="1.17.2"

ADD https://github.com/hadolint/hadolint/releases/download/v${HADOLINT_VERSION}/hadolint-Linux-x86_64 hadolint

RUN apk update \
    && apk add curl \
    && chmod +x hadolint \
    && mv hadolint /usr/local/bin

ENTRYPOINT ["hadolint"]
