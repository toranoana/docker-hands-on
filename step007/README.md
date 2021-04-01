# step007

Railsアプリケーション構築

※ コマンド実行はsourcesディレクトリで行ってください。

## コンテナイメージをビルド

```shell
docker-compose build
```

## イメージを実行

```shell
docker-compose up -d
```

## コンテナ内のコンソールに入る

```shell
docker-compose exec my-app bash
```

## Railsアプリケーションを作成する

```shell
rails new . -d mysql -S -J
```

config/database.yml を開き hostを変更する

```diff
-   host: localhost
+   host: my-database
```

## Railsアプリケーションを起動する

```shell
rails db:create
rails db:migrate
rails server --binding=0.0.0.0
# 停止する場合はCtrl + C
```

Webブラウザで http://localhost:3000 へアクセス

## テーブルを作成し、作成・編集を試す

```
rails generate scaffold user name:string
rails db:migrate
rails server --binding=0.0.0.0
```

Webブラウザで http://localhost:3000/users へアクセス

## コンテナを停止・削除

```shell
# 停止
docker-compose stop

# 削除
docker-compose down
```
