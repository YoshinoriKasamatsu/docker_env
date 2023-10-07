FROM ubuntu:22.04

RUN ["/bin/bash", "-c",  "apt-get update -y && \
                        apt-get upgrade -y && \
                        apt-get install -y curl build-essential gcc make" \
    ]
RUN ["/bin/bash", "-c",  "curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y"]
