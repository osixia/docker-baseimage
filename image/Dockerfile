FROM osixia/light-baseimage:0.2.1
MAINTAINER Bertrand Gouny <bertrand.gouny@osixia.net>

# Install curl less vim-tiny psmisc and clean all
RUN apt-get -y update \
    && LC_ALL=C DEBIAN_FRONTEND=noninteractive apt-get install -y --force-yes --no-install-recommends \
       curl \
       less \
       vim-tiny \
       psmisc \
    && rm -f /etc/dpkg/dpkg.cfg.d/01_nodoc /etc/dpkg/dpkg.cfg.d/01_nolocales \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
