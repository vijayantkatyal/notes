# Docker

```docker-compose build

docker-compose up

docker run --name mysql_server -v mysql_database:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=password -d mysql:latest

docker exec -it mysql_server bash -c "mysql -p"

docker exec -it <name> composer require phpoffice/phpspreadsheet

docker exec -it <name> php artisan migrate
```


```bash
docker run --rm --interactive --tty \
  --volume $PWD:/app \
  composer install
```


> clone laravel version from github

```bash
docker run --rm --interactive --tty \
  --volume $PWD:/app \
  composer install
```

> docker-compose build
> dokcer-compose up