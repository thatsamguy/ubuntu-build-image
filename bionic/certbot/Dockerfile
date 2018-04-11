FROM ubuntu:bionic

ENV DEBIAN_FRONTEND noninteractive

RUN \
  apt-get update && \
  apt-get install -y language-pack-en-base && \
  export LC_ALL=en_US.UTF-8 && \
  export LANG=en_US.UTF-8 && \
  apt-get install -y python-software-properties software-properties-common curl && \
  apt-get install -y python3-pip && \
  pip3 install certbot certbot-route53 && \
  apt-get remove -y python-software-properties software-properties-common && \
  apt-get autoremove -y && \
  rm -rf /var/lib/apt/lists/*