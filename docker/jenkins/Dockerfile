FROM jenkins/jenkins:lts
USER root
RUN apt-get update && \
    apt-get install -y --no-install-recommends \
      docker.io \
      docker-compose \
      git \
      curl && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

RUN groupadd -f docker && \
    usermod -aG docker jenkins

