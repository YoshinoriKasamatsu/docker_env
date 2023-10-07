FROM ubuntu:22.04

RUN ["/bin/bash", "-c",  "apt-get update -y && \
                        apt-get upgrade -y && \
                        apt-get install -y curl build-essential gcc-aarch64-linux-gnu g++-aarch64-linux-gnu make" \
    ]
RUN ["/bin/bash", "-c", "curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y"]
RUN ["/bin/bash", "-c", "source $HOME/.cargo/env && rustup target add aarch64-unknown-linux-gnu"] 
RUN ["/bin/bash", "-c", "echo '[target.aarch64-unknown-linux-gnu]\nlinker = \"aarch64-linux-gnu-gcc\"' >> $HOME/.cargo/config"]
