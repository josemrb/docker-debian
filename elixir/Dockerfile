FROM josemrb/build-asdf:0.6.0-20181102
LABEL maintainer="Jose Miguel Rivero Bruno <work@josemrb.com>"

RUN asdf plugin-add erlang https://github.com/asdf-vm/asdf-erlang.git
ARG ERLANG_VERSION=21.1.1
RUN asdf install erlang $ERLANG_VERSION
RUN asdf global erlang $ERLANG_VERSION

RUN asdf plugin-add elixir https://github.com/asdf-vm/asdf-elixir.git
ARG ELIXIR_VERSION=1.7.4-otp-21
RUN asdf install elixir $ELIXIR_VERSION
RUN asdf global elixir $ELIXIR_VERSION

RUN \
      mix local.hex --force && \
      mix local.rebar --force
