From nvidia/cuda:11.1.1-devel-ubuntu20.04

# author
MAINTAINER Joey Wilson

LABEL version="1"
LABEL description="Container to run Temporal Scene Flow"

RUN apt-get update
RUN DEBIAN_FRONTEND="noninteractive" apt-get -y install tzdata

RUN apt-get update && apt-get install -y --no-install-recommends \
    sudo \
    git \
    emacs \
    wget \
    python3-pip \
    python3-setuptools \
    python3-dev

# Necessary python packages
RUN pip3 install torch==1.8.1+cu111 torchvision==0.9.1+cu111 torchaudio==0.8.1 -f https://download.pytorch.org/whl/torch_stable.html
RUN pip3 install notebook ninja

COPY . .
