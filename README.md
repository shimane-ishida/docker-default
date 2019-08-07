# 個人用開発環境セット

## 概要
Docker-composeを使用してローカル環境を構築します。

### 環境
* dockerコマンドが使用できること
* docker-composeコマンドが使用できること

### セットアップ
プロジェクトルートディレクトリで下記のコマンドを実行

```
docker-compose up -d
```

※最初に立ち上げた際にエラーが発生する可能性があるので、もしエラーが発生した場合は
「docker-compose down」を実行して再度、上記のコマンドでdockerを立ち上げる

### 確認

```
http://localhost
または
http://[docker-composeから払い出されたIPアドレス]
```