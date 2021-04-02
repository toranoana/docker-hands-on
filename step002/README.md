# step002

# Nginx建てる

```shell
docker pull nginx
docker run --name hello-nginx -d -p 81:80 nginx
```

※失敗後82番ポートでやり直す場合

```shell
docker rm hello-nginx -f
docker run --name hello-nginx -d -p 82:80 nginx
```

## コンテナを停止・削除

```shell
# 停止
docker stop hello-nginx

# 削除
docker rm hello-nginx
```
