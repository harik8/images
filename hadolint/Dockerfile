FROM alpine:3.10.3

MAINTAINER "hari.karthigasu@gmail.com"

ARG HADOLINT_VERSION="1.17.2"

RUN apk update \
    && apk add curl

RUN curl -L -o hadolint https://github.com/hadolint/hadolint/releases/download/v${HADOLINT_VERSION}/hadolint-Linux-x86_64 \
    && chmod +x hadolint \
    && mv hadolint /usr/local/bin

ENTRYPOINT ["hadolint"]
    

