ARG ALPINE_VERSION=${ALPINE_VERSION}
FROM alpine:${ALPINE_VERSION}

LABEL description="Docker container for building static sites with the Hugo static site generator."
LABEL maintainer="Tom Wygonik <thomas.wygonik@gmail.com>"

ARG HUGO_VERSION=${HUGO_VERSION}

ADD https://github.com/gohugoio/hugo/releases/download/v${HUGO_VERSION}/hugo_${HUGO_VERSION}_Linux-64bit.tar.gz /tmp
RUN tar -xf /tmp/hugo_${HUGO_VERSION}_Linux-64bit.tar.gz -C /tmp \
    && mkdir -p /usr/local/sbin \
    && mv /tmp/hugo /usr/local/sbin/hugo \
    && rm -rf /tmp/${HUGO_ID}_linux_amd64 \
    && rm -rf /tmp/${HUGO_ID}_Linux-64bit.tar.gz \
    && rm -rf /tmp/LICENSE.md \
    && rm -rf /tmp/README.md