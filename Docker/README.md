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

## コンテナ設定変更
### 削除
```
docker-compose stop
docker-compose down
docker images
docker rmi <イメージID>
```