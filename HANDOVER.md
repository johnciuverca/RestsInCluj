# RestsInCluj Handover

## Current status

The original Spring Boot application runs successfully.

- Java: Temurin 8
- Spring Boot: 1.5.2.RELEASE
- Maven Wrapper: Maven 3.6.0
- PostgreSQL: localhost:5433
- Database: restsInCluj
- User: ciuverca
- Application URL: http://localhost:8090

## Branches

- `master`: original remote project
- `baseline/original-app-runs`: verified runnable baseline

## Local baseline changes

- PostgreSQL port changed from 5432 to 5433.
- PostgreSQL user changed from postgres to ciuverca.
- SQL schema script fixed so it can be imported repeatedly.

## Run the application

```bash
JAVA_HOME=$(/usr/libexec/java_home -v 1.8) bash mvnw spring-boot:run
```

## Database import

```bash
psql -h localhost -p 5433 -U ciuverca -d restsInCluj -f src/main/resources/db_querys.sql
```

Warning: the SQL script drops and recreates local tables.

## Next step

Begin modernization from a new branch, keeping the verified baseline unchanged.
