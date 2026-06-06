FROM ubuntu:26.04

RUN apt update \
    && apt install -y --no-install-recommends \
        ca-certificates \
        sudo \
        python3 \
        python3-venv \
        python-is-python3 \
        golang \
        nodejs \
        openssh-server \
    && apt clean \
    && rm -rf /var/lib/apt/lists/*


WORKDIR /home/ubuntu/app

RUN echo "#1000 ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/devcontainer \
    && chown 1000:1000 -Rv /home/ubuntu

USER 1000

RUN go install github.com/go-delve/delve/cmd/dlv@latest

