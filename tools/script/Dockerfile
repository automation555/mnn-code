FROM nvidia/cuda:11.2.0-cudnn8-devel-ubuntu20.04
ENV DEBIAN_FRONTEND=noninteractive
# install deps
RUN set -x; buildDeps='cmake protobuf-compiler lcov unzip wget git netcat python python3 pip' \
    && echo 'deb http://mirrors.aliyun.com/ubuntu/ focal main restricted universe multiverse\ndeb http://mirrors.aliyun.com/ubuntu/ focal-security main restricted universe multiverse\ndeb http://mirrors.aliyun.com/ubuntu/ focal-updates main restricted universe multiverse\ndeb http://mirrors.aliyun.com/ubuntu/ focal-proposed main restricted universe multiverse\ndeb http://mirrors.aliyun.com/ubuntu/ focal-backports main restricted universe multiverse' > /etc/apt/sources.list \
    && apt-get update \
    && apt-get install -y $buildDeps
# install python deps
RUN set -x; pip install numpy tensorflow torch
