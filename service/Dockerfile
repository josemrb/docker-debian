FROM josemrb/debian:9.5-base-20181102
LABEL maintainer="Jose Miguel Rivero Bruno <work@josemrb.com>"

RUN \
      apt-get update -qq && \
      apt-get install -qq --no-install-recommends \
      dumb-init

ENTRYPOINT ["/usr/bin/dumb-init", "--"]
