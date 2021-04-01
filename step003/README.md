# step003

Nginx建ててみるDocker編2

※ コマンド実行はsourcesディレクトリで行ってください。

## コンテナイメージをビルド

```shell
docker build -t my-nginx .
```

## イメージを実行

```shell
docker run --name hello-nginx -d -p 81:80 my-nginx
```

## コンテナを停止・削除

```shell
# 停止
docker stop hello-nginx

# 削除
docker rm hello-nginx
```
