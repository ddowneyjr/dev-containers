FROM salesforce/cli:latest-full

USER root

RUN apt-get update && apt-get install -y \
    openjdk-21-jdk \
    git \
    curl \
    unzip \
    zip \
    jq \
    vim \
    less \
    ca-certificates \
    && rm -rf /var/lib/apt/lists/*

ENV JAVA_HOME=/usr/lib/jvm/java-21-openjdk-amd64
ENV PATH="${JAVA_HOME}/bin:${PATH}"

WORKDIR /workspaces

CMD ["bash"]