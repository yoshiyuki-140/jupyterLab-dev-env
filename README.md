# JupyterLab-dev-env
My JupyterLab テンプレート


## 使い方

1. このリポジトリをクローン
    ```bash
    git clone https://github.com/yoshiyuki-140/jupyterLab-dev-env
    ```

1. リポジトリへ移動
    ```bash
    cd jupyterLab-dev-env
    ```

1. Dockerコンテナの起動
    ```bash
    docker compose up -d
    ```

1. 作業スペースへのアクセス
   - ブラウザで http://localhost:8888/ へアクセス

1. Dockerコンテナの停止
    ```bash
    docker compose down
    ```


## フォルダ説明
```
.
├── py3                     : Python3のJupyterLab環境
│   ├── Dockerfile          : JupyterLabの環境を構築するためのDockerfile
│   └── root_jupyter        : JupyterLabの設定を永続化させるためのフォルダ
├── workspace               : JupyterLabの作業スペース (外部からファイルを追加するときはここに追加する)
└── docker-compose.yml      : Dockerコンテナの設定ファイル
```

## 参考文献
- [DockerでJupyterLabの環境を作ろう](https://www.idnet.co.jp/column/page_187.html)
    > Dockerfileを純粋なJupyterLabの環境を作るように改変したらうまくいった

