# nginx-proxy-container

nginx proxy 機能をコンテナで実装するためのサンプル。

## setup

```
docker-compose up -d
```

## test

```
docker exec -it test /bin/bash

# http(8080) -> https(443) 変換
curl http://nginx-proxy.com:8080
curl http://nginx-proxy.com:8080/search?q=hogehoge

# https(4443) -> https(443) 変換
curl https://nginx-proxy.com:4443 -k
curl https://nginx-proxy.com:4443/search?q=hogehoge -k
```
