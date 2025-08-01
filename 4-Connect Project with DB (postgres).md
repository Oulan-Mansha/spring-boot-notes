
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
  -p 5433:5432 \
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





# Configure application.properties in spring boot


```
#DB configuration  
spring.datasource.url=jdbc:postgresql://localhost:5433/hospitaldb  
spring.datasource.username=postgres  
spring.datasource.password=pass123  
  
spring.jpa.hibernate.ddl-auto=update  
spring.jpa.show-sql=true

```

### spring.jpa.hibernate.ddl-auto=

 **DDL** = Data Definition Language
Yeh SQL commands hoti hain jo **database structure** (schema) ko define karti hain:

| Command  | Purpose                      |
| -------- | ---------------------------- |
| `CREATE` | Naya table ya column banana  |
| `ALTER`  | Table ko modify karna        |
| `DROP`   | Table ya column delete karna |






