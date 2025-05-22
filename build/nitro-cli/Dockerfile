FROM amazonlinux:2023

RUN dnf update -y
# Install nitro-cli dependencies
RUN dnf install -y \
    aws-nitro-enclaves-cli \
    aws-nitro-enclaves-cli-devel \
    tar \
    unzip \
    curl-minimal \
    jq \
    shadow-utils \
    && dnf clean all

# Add enclaver system user
RUN useradd -m enclaver

WORKDIR /build

ENTRYPOINT ["nitro-cli"]

