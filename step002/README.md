# step002

Nginx建ててみるDocker編1

```shell
docker run --name hello-nginx -d -p 81:80 nginx
```

失敗後82番ポートでやり直す場合

```shell
docker rm hello-nginx -f
docker run --name hello-nginx -d -p 82:80 nginx
```
