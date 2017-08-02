Debian - PostgreSQL9.6 (日本環境）

オフィシャルのPostgreSQLを元に日本環境の調整を行いました。

### 調整内容 ###

* locale設定 (ja.utf-8)
* タイムゾーン （Asia/Tokyo）
* 必要なツールのインストール
 

### 使い方 ###

下記のコマンドにてコンテナを起動します

```
$ docker pull reflet/debian8-postgre96
$ docker run --rm -u "postgres" -it reflet/debian8-postgre96 bash
```

### メンテナンス ###

下記のコマンドにてソースのダウンロードとイメージの構築を実行します。

```
$ git clone git@bitbucket.org:reflet/docker-debian8-postgre96.git .
$ docker build -t reflet/debian8-postgre96 .
$ docker login
$ docker tag reflet/debian8-postgre96 reflet/debian8-postgre96:{tag}
$ docker push reflet/debian8-postgre96
```

