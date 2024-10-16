FROM --platform=linux/arm64 ubuntu:20.04

# Install dependencies for Go and Python
# psmiscはpstreeを使えるようにするため
# man-dbはmanコマンドを使用できるようにするため
RUN apt-get update && apt-get install -y \
    curl \
    build-essential \
    python3 \
    python3-pip \
    python3-venv \
    python-is-python3 \
    git \
    wget \
    libc6 \
    psmisc \
    vim \
    man-db \
    && rm -rf /var/lib/apt/lists/*

# Install Go
RUN wget https://golang.org/dl/go1.17.3.linux-arm64.tar.gz \
    && tar -C /usr/local -xzf go1.17.3.linux-arm64.tar.gz \
    && rm go1.17.3.linux-arm64.tar.gz

# Set environment variables for Go
ENV PATH="/usr/local/go/bin:${PATH}"

# Create a working directory
WORKDIR /app

# Ref: https://qiita.com/ssc-ynakamura/items/d69307a3d94bf81c363d
# システムの最小化を解除するため。(これがないとmanコマンドとかが使えない)
RUN yes | unminimize

# ネットワーク系のシステムコールを呼ぶかもしれないため
EXPOSE 8080
