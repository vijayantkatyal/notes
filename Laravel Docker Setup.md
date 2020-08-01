# Laravel Docker Setup

clone laravel from github

install dependencies using composer image

```bash
docker run --rm --interactive --tty \
  --volume $PWD:/app \
  composer install
```

or

```bash
docker run --rm --interactive --tty \
  --volume $PWD:/app \
  composer create-project --prefer-dist laravel/laravel <project name>
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

