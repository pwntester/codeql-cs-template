ARG VARIANT="3.8"
FROM mcr.microsoft.com/vscode/devcontainers/python:0-${VARIANT}

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive && apt-get -y install --no-install-recommends fuse
RUN wget https://github.com/github/codeql-cli-binaries/releases/latest/download/codeql-linux64.zip -O codeql.zip && \
  unzip -q codeql.zip && \
  rm codeql.zip && \
  mv codeql /opt
ENV PATH="/opt/codeql:${PATH}"
