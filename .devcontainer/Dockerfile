# Ubuntu 22.04 をベースとした Dev Container
FROM mcr.microsoft.com/devcontainers/base:ubuntu-22.04

# パッケージのインストール（Java 17, Git, Vim, 便利ツール、日本語ロケール）
RUN apt-get update && \
    apt-get install -y \
        openjdk-17-jdk \
        maven \
        git \
        vim \
        curl \
        wget \
        zip \
        unzip \
        less \
        locales && \
    locale-gen ja_JP.UTF-8

# 日本語ロケール設定
ENV LANG=ja_JP.UTF-8 \
    LANGUAGE=ja_JP:ja \
    LC_ALL=ja_JP.UTF-8

# 作業ディレクトリ
WORKDIR /workspaces/demo

# Java のバージョン確認
RUN java -version && mvn -v