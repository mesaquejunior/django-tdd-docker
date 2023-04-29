# django-tdd-docker

## Build docker image
docker-compose up -d --build

## Run migrations
docker-compose exec movies python manage.py migrate --noinput

## Connect to pgsql db
docker-compose exec movies-db psql --username=movies --dbname=movies_dev

## List docker volume
docker volume inspect django-tdd-docker_postgres_data