# ベースイメージを指定
FROM mcr.microsoft.com/devcontainers/base:ubuntu-22.04

# 必要なパッケージをインストール
RUN apt-get update && apt-get install -y \
    curl \
    build-essential \
    libssl-dev \
    pkg-config \
    nodejs \
    npm \
    && rm -rf /var/lib/apt/lists/*

# Rustのインストール
RUN curl https://sh.rustup.rs -sSf | sh -s -- -y
ENV PATH="/root/.cargo/bin:${PATH}"

# Node.jsのバージョン確認と更新
RUN npm install -g n && n stable

# 作業ディレクトリを設定
WORKDIR /workspace
