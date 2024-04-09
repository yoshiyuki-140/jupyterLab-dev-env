FROM python:3.11.8-bullseye
ARG DEBIAN_FRONTEND=noninteractive

# パッケージの追加とタイムゾーンの設定
# 必要に応じてインストールするパッケージを追加してください
RUN apt-get update && apt-get install -y \
    tzdata \
    &&  ln -sf /usr/share/zoneinfo/Asia/Tokyo /etc/localtime \
    &&  apt-get clean \
    &&  rm -rf /var/lib/apt/lists/*

ENV TZ=Asia/Tokyo

WORKDIR /workspace
COPY ./requirements.txt /workspace/requirements.txt

# requirements.txtの内容を読み込む
RUN python3 -m pip install --upgrade pip \
    &&  pip install --no-cache-dir \
    -r /workspace/requirements.txt
