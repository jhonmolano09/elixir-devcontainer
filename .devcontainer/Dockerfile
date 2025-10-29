# Use an official Erlang image as the base
FROM erlang:28.1-alpine

# Environment variables
ENV LANG=C.UTF-8 \
    ELIXIR_VERSION=1.19.1 \
    MIX_HOME=/opt/mix \
    HEX_HOME=/opt/hex

# Install build dependencies
RUN apk add --no-cache \
    bash \
    git \
    curl \
    build-base \
    openssl-dev \
    ncurses-dev \
    inotify-tools

# Install Elixir
RUN wget https://github.com/elixir-lang/elixir/releases/download/v${ELIXIR_VERSION}/elixir-otp-28.zip && \
    unzip elixir-otp-28.zip -d /usr/local && \
    rm elixir-otp-28.zip

# Add Elixir binaries to PATH
ENV PATH="/usr/local/bin:${PATH}"

# Install Hex and Rebar
RUN mix local.hex --force && \
    mix local.rebar --force

# Install Expert LSP (nightly build)
RUN wget https://github.com/elixir-lang/expert/releases/download/nightly/expert_linux_amd64 -O /usr/local/bin/expert && \
    chmod +x /usr/local/bin/expert

# Set working directory
WORKDIR /workspace

# Install Phoenix 
RUN mix archive.install hex phx_new --force
# Install Credo
RUN mix archive.install hex credo --force

# Create mix cache directories
RUN mkdir -p ${MIX_HOME} ${HEX_HOME}
