# Copyright (c) 2016-2025 Crave.io Inc. All rights reserved
FROM accupara/ubuntu:14.04

RUN set -x \
 && sudo ln -svf /bin/bash /bin/sh \
 && sudo apt-get update \
 && sudo apt-get install -y \
        bison \
        build-essential \
        curl \
        gawk \
        gettext \
        libc6-dev \
        libc-dev \
        libz-dev \
        ncurses-dev \
        openjdk-6-jdk \
        patch \
        subversion \
        texinfo \
        wget
ADD ["mnt", "/mnt/"]
RUN cd /mnt && make setup
RUN cd /mnt && . ~/.bashrc && make sources
