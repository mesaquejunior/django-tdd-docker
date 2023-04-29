# django-tdd-docker

## Build docker enviroment
docker-compose up -d --build

## Destroy enviroment
docker compose down -v

## Run migrations
docker-compose exec movies python manage.py migrate --noinput

## Connect to pgsql db
docker-compose exec movies-db psql --username=movies --dbname=movies_dev

## List docker volume
docker volume inspect django-tdd-docker_postgres_data

## Run tests
docker-compose exec movies pytest