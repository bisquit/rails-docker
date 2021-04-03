```sh
docker-compose run web bundle exec rails new . --api

docker-compose build

docker-compose up
```

```sh
docker-compose exec web bash

bin/rails db:setup
bin/rails db:migrate
```
