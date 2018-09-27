FROM debian:stretch
LABEL maintainer="Jose Miguel Rivero Bruno <work@josemrb.com>"

ENV \
  DEBIAN_FRONTEND=noninteractive \
  LC_ALL=C \
  TERM=linux

RUN \
      apt-get update -qq && \
      apt-get install -qq --no-install-recommends \
      apt-utils \
      apt-transport-https \
      ca-certificates \
      software-properties-common

RUN \
      apt-get install -qq --no-install-recommends locales && \
      echo "en_US.UTF-8 UTF-8" > /etc/locale.gen && \
      locale-gen en_US.UTF-8 UTF-8 && \
      update-locale LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_CTYPE=en_US.UTF-8 LC_ALL=en_US.UTF-8

ENV \
  LANG=en_US.UTF-8 \
  LANGUAGE=en_US:en \
  LC_CTYPE=en_US.UTF-8 \
  LC_ALL=en_US.UTF-8

RUN apt-get install -qq --no-install-recommends \
      curl \
      git \
      less \
      lsof \
      procps \
      psmisc \
      sudo \
      vim-tiny \
      unzip && \
      ln -s /usr/bin/vim.tiny /usr/bin/vim

SHELL ["/bin/bash", "-c"]
ENTRYPOINT ["/bin/bash"]
