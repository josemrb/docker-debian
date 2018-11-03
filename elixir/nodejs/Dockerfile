FROM josemrb/elixir:1.7.4-otp-21-20181102
LABEL maintainer="Jose Miguel Rivero Bruno <work@josemrb.com>"

RUN asdf plugin-add nodejs https://github.com/asdf-vm/asdf-nodejs.git

RUN /build/.asdf/plugins/nodejs/bin/import-release-team-keyring

ARG NODEJS_VERSION=10.13.0
RUN asdf install nodejs  $NODEJS_VERSION
RUN asdf global nodejs $NODEJS_VERSION
