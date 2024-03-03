# JupyterLab-dev-env
このリポジトリは自分用のJupyterLab開発環境テンプレートです。


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
├── conf                    : Python3のJupyterLab環境
│   ├── Dockerfile          : JupyterLabの環境を構築するためのDockerfile
│   └── root_jupyter        : JupyterLabの設定を永続化させるためのフォルダ
├── workspace               : JupyterLabの作業スペース (外部からファイルを追加するときはここに追加する)
└── docker-compose.yml      : Dockerコンテナの設定ファイル
```

### 重要なフォルダ
- `workspace` : 
    JupyterLabの作業スペース、データセットやソースコードの置き場所
- `conf/root_jupyter` : 
    JupyterLabの設定ファイルが入っている、dockerコンテナを落としてもここにファイルがあるのでフォントの変更やフォーマッターの指定等の設定は消えない

## 参考文献
- [DockerでJupyterLabの環境を作ろう](https://www.idnet.co.jp/column/page_187.html)
    > 本リポジトリでは、ベースイメージのバージョンをPython3.9系から3.11.8のDebian系にしている。
- [Docker実践ガイド: コンテナ環境の構築・運用・活用](https://ndlsearch.ndl.go.jp/books/R100000002-I032642811)    

