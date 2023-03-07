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
    
RUN apt-get update && \
    apt-get install -y software-properties-common && \
    apt-add-repository -y non-free && \
    apt-get update && \
    apt-get install -y intel-media-va-driver-non-free ffmpeg && \
    rm -rf /var/lib/apt/lists/*

ENV NEXTCLOUD_UPDATE=1

COPY start.sh /
RUN ["chmod", "+x", "/start.sh"]
CMD /start.sh