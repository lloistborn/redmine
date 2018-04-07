# Redmine

### What is Redmine?
![redmine](https://raw.githubusercontent.com/docker-library/docs/969091c4c590befe236a71d4a7bce5823fff020d/redmine/logo.png)

Redmine is a free and open source, web-based project management and issue tracking tool. It allows users to manage multiple projects and associated subprojects. It features per project wikis and forums, time tracking, and flexible role based access control. It includes a calendar and Gantt charts to aid visual representation of projects and their deadlines. Redmine integrates with various version control systems and includes a repository browser and diff viewer.

> [wikipedia.org/wiki/Redmine](wikipedia.org/wiki/Redmine)

### Official docker images

Postgresql `postgres:10-alpine`

Redmine `redmine:latest`

### Run using docker compose
```docker-compose -f docker-compose.yml up```

# Environment Variables

## Redmine
When you start the redmine image, you can adjust the configuration of the instance by passing one or more environment variables on the docker run command line. The default user with administrator role is `admin` and password `admin`.

### `REDMINE_DB_POSTGRES`
These variable allow you to set the hostname or IP address of the PostgreSQL host, respectively. The values are mutually exclusive so it is undefined behavior if both are set. If NO variable is set, the image will fall back to using SQLite.

## Postgresql

### `POSTGRES_PASSWORD`
This environment variable is recommended for you to use the PostgreSQL image. This environment variable sets the superuser password for PostgreSQL. The default superuser is defined by the `POSTGRES_USER` environment variable.

### `POSTGRES_USER`
This optional environment variable is used in conjunction with POSTGRES_PASSWORD to set a user and its password. This variable will create the specified user with superuser power and a database with the same name. If it is not specified, then the default user of `postgres` will be used.
