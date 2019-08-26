## 実行

1. $ docker-compose run --rm server rails new .
2. database.ymlを書き換える
3. $ docker-compose run --rm server bundle exec rails db:create
4. $ docker-compose run --rm web create-react-app /app --typescript
5. $ docker-compose up -d
6. $ docker-compose exec web npm run build

多分これでいける


database.ymlを
```
  password: docker
  host: mysql
```

に変更する

## コマンドの実行

```
$ docker-compose exec [container_name] [command]
```
例) serverコンテナでls -alを実行する
``` $ docker-compose exec server ls -al ```