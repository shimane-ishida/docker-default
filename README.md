# 個人用開発環境セット

## 概要
Docker-composeを使用してローカル環境を構築します。

### 環境
* dockerコマンドが使用できること
* docker-composeコマンドが使用できること
* composerコマンドが使用できること

### セットアップ
プロジェクトルートディレクトリで下記のコマンドを実行

```
docker-compose up -d
```

※最初に立ち上げた際にエラーが発生する可能性があるので、もしエラーが発生した場合は
「docker-compose down」を実行して再度、上記のコマンドでdockerを立ち上げる

###依存ライブラリのインストール
プロジェクトルートディレクトリで下記のコマンドを実行

```
composer install
```

### データベースのマイグレーション
プロジェクトルートディレクトリで下記のコマンドを実行

```
mv phinx.yml.org phinx.yml
```
phinx.ymlを利用環境にあわせて編集

* マイグレーション

```
./vendor/bin/phinx migrate
```

* 初期データの投入

```
./vendor/bin/phinx seed:run
または
https://localhost/restore.php
https://[docker-composeから払い出されたIPアドレス]/restore.php
```

### 確認

```
https://localhost
または
https://[docker-composeから払い出されたIPアドレス]
```