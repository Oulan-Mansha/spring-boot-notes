
# Installation of postgre sql database using docker

#### Pull docker image

```
docker pull postgres
```

#### Run postgreSQL Container

```

docker run --name hospital-postgres \
  -e POSTGRES_USER=postgres \
  -e POSTGRES_PASSWORD=pass123 \
  -e POSTGRES_DB=hospitaldb \
  -p 5432:5432 \
  -d postgres

```

| Setting          | Value               |
| ---------------- | ------------------- |
| DB Username      | `postgres`          |
| DB Password      | `pass123`           |
| DB Name          | `hospitaldb`        |
| Docker Container | `hospital-postgres` |
| Exposed Port     | `5432`              |

#### Verify it's running

```
docker ps
```

#### Connect to PostgreSQL CLI

```
docker exec -it hospital-postgres psql -U postgres -d hospitaldb
```



#
