FROM salesforce/cli:latest-full

USER root

RUN apt-get update && apt-get install -y \
    git \
    curl \
    unzip \
    zip \
    jq \
    vim \
    less \
    ca-certificates \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /workspaces

CMD ["bash"]