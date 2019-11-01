FROM alpine:3.10.3

LABEL MAINTAINER "hari.karthigasu@gmail.com"

ARG HADOLINT_VERSION="1.17.2"

ADD https://github.com/hadolint/hadolint/releases/download/v${HADOLINT_VERSION}/hadolint-Linux-x86_64 hadolint

RUN chmod +x hadolint \
    && mv hadolint /usr/local/bin
