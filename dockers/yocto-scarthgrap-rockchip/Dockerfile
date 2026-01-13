FROM ubuntu:24.04

RUN apt-get update && \
apt-get install -y vim git python3 gcc cmake make gzip unzip \
locales bzip2 chrpath cpio diffstat file g++ gawk \
lz4 wget zstd

RUN locale-gen en_US.UTF-8

RUN useradd -m -u 1001 -U -s /bin/bash user

USER user
WORKDIR /home/user

RUN git clone  --branch scarthgap https://github.com/yoctoproject/poky.git /home/user/poky && \
cd /home/user/poky && \
git checkout 72983ac391008ebceb45edc7a8f0f6d5f4fe715c 

RUN git clone  --branch scarthgap https://github.com/openembedded/meta-openembedded.git /home/user/poky/meta-openembeeded && \
cd /home/user/poky/meta-openembeeded && \
git checkout 2b26d30fc7f478f5735d514f0c1bc28f6a4148b6

RUN git clone  --branch scarthgap https://github.com/JeffyCN/meta-rockchip.git /home/user/poky/meta-rockchip && \
cd /home/user/poky/meta-rockchip && \
git checkout 194486dc7f8dda9bc6dae3e006d703df2f99ea47


