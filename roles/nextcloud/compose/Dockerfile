FROM nextcloud:stable-apache

RUN set -ex; \
    \
    apt-get update; \
    apt-get install -y --no-install-recommends \
        ffmpeg \
        ghostscript \
        libmagickcore-6.q16-6-extra \
        procps \
    ; \
    rm -rf /var/lib/apt/lists/*
    
ENV NEXTCLOUD_UPDATE=1