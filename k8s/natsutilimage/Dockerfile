FROM ubuntu:24.04

LABEL org.opencontainers.image.description See https://github.com/natpowning/natpowning/blob/main/k8s/natsutilimage/README.md

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
    apt-get install -y \
    zsh \
    curl \
    wget \
    git \
    dnsutils \
    iputils-ping \
    net-tools \
    iproute2 \
    vim \
    python3 \
    htop \
    lsof \
    tcpdump \
    telnet \
    jq \
    unzip \
    && apt-get clean

# Install Oh My Zsh
RUN sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" "" --unattended

# Set zsh as the default shell
RUN chsh -s $(which zsh)

# myconfigs is at the root of the natpowning repsoitory which should be what's used for build context
COPY myconfigs/vimrc /root/.vimrc

WORKDIR /root

CMD ["zsh"]
