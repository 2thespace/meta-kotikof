FROM ubuntu:24.04

RUN apt-get update && \
apt-get install -y  vim git python3 gcc cmake make gzip unzip locales       \
bzip2 chrpath cpio diffstat file g++ gawk lz4 wget zstd ssh gcc-multilib    \
g++-multilib module-assistant expect texinfo libssl-dev bison flex fakeroot  \
gperf autoconf device-tree-compiler libncurses5-dev pkg-config bc            \
python-is-python3 passwd openssl openssh-server openssh-client rsync


RUN locale-gen en_US.UTF-8

RUN git clone https://github.com/LuckfoxTECH/luckfox-pico.git

RUN useradd -m -u 1001 -U -s /bin/bash user

USER user
WORKDIR /home/user

