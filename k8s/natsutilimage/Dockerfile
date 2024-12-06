FROM ubuntu:24.04

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
    nano \
    htop \
    lsof \
    tcpdump \
    telnet \
    jq \
    unzip \
    && apt-get clean

# Install Oh My Zsh
RUN sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" "" --unattended

# Install Oh My Posh
RUN wget https://github.com/JanDeDobbeleer/oh-my-posh/releases/latest/download/posh-linux-amd64 -O /usr/local/bin/oh-my-posh && \
    chmod +x /usr/local/bin/oh-my-posh

# Set zsh as the default shell
RUN chsh -s $(which zsh)

# These are at the root of the natpowning repsoitory which should be what's used for build context
COPY myconfigs/vimrc /root/.vimrc
COPY myconfigs/zshrc /root/.zshrc

# Set up Oh My Posh in the zsh configuration
RUN echo 'eval "$(oh-my-posh init zsh --config /root/.poshthemes/your-theme.omp.json)"' >> /root/.zshrc

WORKDIR /root

CMD ["zsh"]
