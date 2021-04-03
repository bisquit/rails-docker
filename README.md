## Scaffold rails

```bash
docker-compose run web bundle exec rails new . --force
```

+ mysql
```sh
docker-compose run web bundle exec rails new . --force --database=mysql
```

+ api mode
```bash
docker-compose run web bundle exec rails new . --force --database=mysql --api
```

## Build docker image and up

```sh
docker-compose build

docker-compose up
```

## Initialize rails db

```sh
docker-compose exec web bash

bin/rails db:setup
bin/rails db:migrate
```
