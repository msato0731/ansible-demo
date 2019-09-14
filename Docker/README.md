## スタート
```
docker-compose up -d
```

## ストップ
```
docker-compose stop
```

## controllerログイン(ansible実行側)
```
docker-compose exec controller /bin/bash
```

## targetログイン(ansible設定適用される側)
```
docker-compose exec target /bin/bash
```

## コンテナ削除
```
docker-compose down
```

## イメージ削除
```
docker images
docker rmi <イメージID>
```

## targetへhttpアクセス
```
http://localhost:8080/
```