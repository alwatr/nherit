FROM ghcr.io/alwatr/nherit:4.18.0

# Override default environment for static websites
ENV NGINX_CLIENT_MAX_BODY_SIZE=1k \
    NGINX_OPEN_FILE_CACHE="max=1000 inactive=1h" \
    NGINX_OPEN_FILE_CACHE_VALID=1M \
    NGINX_EXPIRES_STATIC=max \
    NGINX_LIMIT_REQ_RATE=400

ARG BUILD_REV
ARG BUILD_DATE
ARG BUILD_VERSION=dev
ENV IMAGE_VERSION=$BUILD_VERSION \
    IMAGE_REVISION=$BUILD_REV
LABEL org.opencontainers.image.title="alwatr/nherit:ws" \
      org.opencontainers.image.description="This is a high-performance version of NGINX, which has been enhanced by Alwatr for the purpose of serving static website content efficiently." \
      org.opencontainers.image.base.name="ghcr.io/alwatr/nherit:4.18.0" \
      org.opencontainers.image.version="4.18.0" \
      org.opencontainers.image.ref.name="4.18.0-nginx1.31.9-alpine-otel" \
      org.opencontainers.image.licenses="MPL-2.0" \
      org.opencontainers.image.created=${BUILD_DATE} \
      org.opencontainers.image.revision=${BUILD_REV} \
      org.opencontainers.image.vendor="Alwatr" \
      org.opencontainers.image.source="https://github.com/Alwatr/nherit" \
      org.opencontainers.image.url="https://github.com/Alwatr/nherit" \
      org.opencontainers.image.documentation="https://github.com/Alwatr/nherit" \
      org.opencontainers.image.authors="S. Ali Mihandoost <ali.mihandoost@gmail.com> (https://ali.mihandoost.com)"
