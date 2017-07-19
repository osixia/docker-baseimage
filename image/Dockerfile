FROM osixia/light-baseimage:1.1.0
MAINTAINER Bertrand Gouny <bertrand.gouny@osixia.net>

# Install curl less vim-tiny psmisc and clean all
RUN rm -f /etc/dpkg/dpkg.cfg.d/01_nodoc /etc/dpkg/dpkg.cfg.d/01_nolocales \
    && apt-get -y update \
    && LC_ALL=C DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends \
       curl \
       less \
       vim-tiny \
       psmisc \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
