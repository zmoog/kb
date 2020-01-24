# Docker

## PostgreSQL

How to run a PostgreSQL database using a Docker container.

```bash
$ docker run --name pg-docker -e POSTGRES_PASSWORD=docker -d -p 5432:5432 postgres:9.6   
```

You can also use a volume to persist the data outside the container.

```bash
$ mkdir -p ~/docker/volumes/postgres
$ docker run --rm --name pg-docker -e POSTGRES_PASSWORD=docker -d -p 5432:5432 -v ~/docker/volumes/postgres:/var/lib/postgresql/data postgres:9.6
```
