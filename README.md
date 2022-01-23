## Scaffold rails

basic (sqlite)
```bash
docker-compose run web bundle exec rails new . --force
```

db mysql
```sh
docker-compose run web bundle exec rails new . --force --database=mysql
```

api mode
```bash
docker-compose run web bundle exec rails new . --force --database=mysql --api
```

## Modify database config

config/database.yml

```diff
- password
- host: localhost
+ password: password
+ host: db
```

## Build docker image and up

```sh
docker-compose build

docker-compose up
```

※ For M1 Mac, use mariadb instead.

docker-compose.yml
```diff
- image: mysql:8.0
+ image: mariadb
```

## Create db tables

```sh
docker-compose exec web bash

bin/rails db:prepare
```

## (Optional) Use sidekiq

use `docker-compose.sidekiq.yml`.

Before `docker-compose up`, install sidekiq

```
docker-compose run web bundle add sidekiq
```
