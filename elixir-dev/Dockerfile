FROM tpdock/alpine-elixir:1.4.2

RUN apk --update add erlang-crypto erlang-syntax-tools erlang-parsetools \
      erlang-inets erlang-ssl erlang-public-key erlang-eunit erlang-xmerl \
      erlang-edoc erlang-tools erlang-mnesia erlang-runtime-tools \
      erlang-asn1 erlang-sasl erlang-erl-interface erlang-dev \
      gcc wget git openssh make bash grep && \
    sed -i -e 's/4/5/g' /etc/apk/repositories
    apk update && \
    apk upgrade && \
    apk --update add musl-dev \
    rm -rf /var/cache/apk/* && \
    mix local.hex --force && \
    mix local.rebar --force
