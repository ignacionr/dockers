# Use the Official Ubuntu image
FROM ubuntu:23.04

# Set the environment to non-interactive to avoid prompts
ENV DEBIAN_FRONTEND=noninteractive

# Install Python, pip, Conan, libgmock-dev, and mosquitto
RUN apt-get update && \
    apt upgrade -y && \
    apt-get install -y \
    curl software-properties-common python3 python3-pip libgmock-dev mosquitto libmosquitto1 ninja-build \
    gcc-13 git cmake sudo curl libssl-dev gdb unzip awscli libmosquitto-dev tclsh && \
    rm -rf /var/lib/apt/lists/*

# Cleanup
RUN apt-get clean && \
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
