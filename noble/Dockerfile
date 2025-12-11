FROM ubuntu:24.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update -y && \
    apt-get upgrade -y

RUN ln -fs /usr/share/zoneinfo/UTC /etc/localtime && \
    apt-get install --no-install-recommends tzdata -y  && \
    dpkg-reconfigure --frontend noninteractive tzdata

RUN apt-get install -y --no-install-recommends \
    apt-utils \
    build-essential \
    ca-certificates \
    curl \
    dkms \
    gnupg \
    less \
    nano \
    openssh-server \
    openssh-client \
    software-properties-common \
    supervisor \
    sudo \
    unzip \
    wget \
    zip

RUN echo 'ubuntu ALL=(ALL:ALL) NOPASSWD:ALL' > /etc/sudoers.d/ubuntu && \
    chmod 440 /etc/sudoers.d/ubuntu

WORKDIR /home/ubuntu

USER ubuntu