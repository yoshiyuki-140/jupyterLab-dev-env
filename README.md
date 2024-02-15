# JupyterLab-dev-env
JupyterLabの開発環境


## 使い方

### 1. Dockerコンテナの起動
```bash
docker compose up -d
```

### 2. 作業スペースへのアクセス
- ブラウザで http://localhost:8888/ へアクセス

### 3. Dockerコンテナの停止
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
├── docker-compose.yml      : Dockerコンテナの設定ファイル
└── up-down.cmd             : Dockerコンテナの起動と停止を行うバッチファイル
```

## 参考文献
- [DockerでJupyterLabの環境を作ろう](https://www.idnet.co.jp/column/page_187.html)
    > Dockerfileを純粋なJupyterLabの環境を作るように改変したらうまくいった

