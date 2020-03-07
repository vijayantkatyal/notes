# Laravel Docker Setup

clone laravel from github

install dependencies using composer image

```bash
docker run --rm --interactive --tty \
  --volume $PWD:/app \
  composer install
```

install docker compose and webserver file

build docker image

```bash
docker-compose build
```

docker-compose up

```bash
dokcer-compose up
```

