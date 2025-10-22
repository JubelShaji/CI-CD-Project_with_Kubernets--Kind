FROM jenkins/jenkins:lts

USER root

# Install Docker CLI, Node.js v20, and Docker Compose plugin manually
RUN apt-get update && \
    apt-get install -y \
        curl \
        gnupg2 \
        ca-certificates \
        apt-transport-https \
        docker.io && \
    curl -fsSL https://deb.nodesource.com/setup_20.x | bash - && \
    apt-get update && \
    apt-get install -y nodejs && \
    npm install -g npm@latest && \
    apt-get install -y openssh-client && \
    apt-get clean && rm -rf /var/lib/apt/lists/*
