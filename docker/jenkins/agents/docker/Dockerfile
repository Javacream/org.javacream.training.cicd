FROM jenkins/inbound-agent:latest-jdk21

USER root

RUN apt-get update && \
    apt-get install -y \
        git \
        maven \
        docker.io \
        curl \
        unzip && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*
