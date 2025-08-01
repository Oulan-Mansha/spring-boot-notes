
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

#### **DDL** = Data Definition Language
Yeh SQL commands hoti hain jo **database structure** (schema) ko define karti hain:

| Command  | Purpose                      |
| -------- | ---------------------------- |
| `CREATE` | Naya table ya column banana  |
| `ALTER`  | Table ko modify karna        |
| `DROP`   | Table ya column delete karna |
|          |                              |

#### Hibernate `ddl-auto` ke Options:

|Option|Explanation|
|---|---|
|`none`|⚠️ Kuch bhi automatically nahi hoga. Tumhe manually DB schema create karna padega.|
|`validate`|✅ Entity classes aur existing DB schema ko **compare** karega. Agar mismatch mila to **error throw** karega.|
|`update`|✅ Automatically schema ko update karega. Naye columns add karega, lekin existing data ko **delete nahi karega**.|
|`create`|❌ Har baar app run hone par purana schema **delete** karke naya banata hai. Data chala jata hai.|
|`create-drop`|App start pe table create, aur app band hote hi table **drop** (delete) ho jata hai. Mostly testing ke liye.|
|`auto` (deprecated)|Old version ka keyword hai, use nahi karna chahiye.|

#### Real World Mein Kya Use Karna Chahiye?

|Environment|Recommended ddl-auto|
|---|---|
|**Development**|`update`|
|**Testing**|`create-drop`|
|**Production**|`none` ya `validate` (schema manually banate hain)|





