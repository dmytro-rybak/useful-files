## If error: port address already in use
```shell
sudo lsof -i :<port>
```
```shell
sudo kill <process_id>
```

## Run PostgreSQL in Docker
<hr/>

```shell
docker run --name postgres_db -p 5432:5432 -d -e POSTGRES_DB="db" -e POSTGRES_USER="admin" -e POSTGRES_PASSWORD="admin" postgres:latest 
```
<hr/>

## Run Redis in Docker
<hr/>

```shell
docker run --name redis -p 6379:6379 -d redis:latest
```
<hr/>

## Run RabbitMQ in Docker
<hr/>

```shell
docker run --name rabbit -p 5672:5672 -d rabbitmq:latest
```
<hr/>

## Run MongoDB in Docker
<hr/>

```shell
docker run --name mongo_db -p 27017:27017 -d -e MONGO_INITDB_ROOT_USERNAME="admin" -e MONGO_INITDB_ROOT_PASSWORD="admin" -e MONGO_INITDB_DATABASE="db" mongo:latest
```
<hr/>
