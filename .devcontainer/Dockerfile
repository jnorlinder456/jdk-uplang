FROM mcr.microsoft.com/devcontainers/base:ubuntu-22.04

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends git libfreetype6-dev build-essential libfontconfig-dev libcups2-dev libx11-dev libxext-dev libxrender-dev libxrandr-dev libxtst-dev libxt-dev libasound2-dev libffi-dev autoconf zip grep file gdb

# extra for Docker-dev
USER vscode
WORKDIR /home/vscode
RUN wget https://download.java.net/java/GA/jdk21.0.1/415e3f918a1f4062a0074a2794853d0d/12/GPL/openjdk-21.0.1_linux-x64_bin.tar.gz
RUN tar -xvf openjdk-21.0.1_linux-x64_bin.tar.gz
RUN rm openjdk-21.0.1_linux-x64_bin.tar.gz

## Post install
