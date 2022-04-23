# Setup with Docker

## Requirements

- SSH Access
- Docker
- Docker Compose

## Install

Clone the projects from the git repository and start the container with `docker-compose up`. For an update check out the new files from the git repository and restart the container.

[Env Vars](env.md)

### Example

```ini
// .env

COMPOSE_PROJECT_NAME=example

DATABASE_SERVER=db
DATABASE_PORT=3306
DATABASE_NAME=app
DATABASE_USER=admin
DATABASE_PASSWORD=password
DATABASE_ROOT_PASSWORD=password

APP_ENV=prod
APP_SECRET=secret
JWT_PASSPHRASE=passphrase
CORS_ALLOW_ORIGIN='^https?://(localhost|DOMAIN)(:[0-9]+)?$'

VUE_APP_API=DOMAIN
VUE_APP_I18N_LOCALE=en-US
VUE_APP_I18N_FALLBACK_LOCALE=en-US
VUE_APP_BASE_URL=/
```

```yaml
// docker-compose.yml

version: "3.8"

services:
  db:
    image: mysql:8
    command: --default-authentication-plugin=mysql_native_password
    restart: unless-stopped
    environment:
      - MYSQL_DATABASE=${DATABASE_NAME}
      - MYSQL_USER=${DATABASE_USER}
      - MYSQL_PASSWORD=${DATABASE_PASSWORD}
      - MYSQL_ROOT_PASSWORD=${DATABASE_ROOT_PASSWORD}
    volumes:
      - mysql:/var/lib/mysql

  php-fpm:
    build:
      context: ./apps/core
      dockerfile: docker/php-fpm/Dockerfile
    restart: unless-stopped
    depends_on:
      - db
    environment:
      - APP_ENV=${APP_ENV}
      - APP_SECRET=${APP_SECRET}
      - DATABASE_SERVER=${DATABASE_SERVER}
      - DATABASE_PORT=${DATABASE_PORT}
      - DATABASE_URL=mysql://${DATABASE_USER}:${DATABASE_PASSWORD}@${DATABASE_SERVER:-db}:${DATABASE_PORT:-3306}/${DATABASE_NAME}?serverVersion=8.0
      - JWT_PASSPHRASE=${JWT_PASSPHRASE}
      - CORS_ALLOW_ORIGIN=${CORS_ALLOW_ORIGIN}
    volumes:
      - jwt:/usr/local/apache2/htdocs/config/jwt
      - data:/usr/local/apache2/htdocs/data

  core:
    build:
      context: ./apps/core/docker/httpd
    restart: unless-stopped
    depends_on:
      - php-fpm
    ports:
      - 9001:80

  web:
    build:
      context: ./apps/web
      args:
        - VUE_APP_API=${VUE_APP_API}
        - VUE_APP_I18N_LOCALE=${VUE_APP_I18N_LOCALE}
        - VUE_APP_I18N_FALLBACK_LOCALE=${VUE_APP_I18N_FALLBACK_LOCALE}
        - VUE_APP_BASE_URL=${VUE_APP_BASE_URL}
    restart: unless-stopped
    ports:
      - 9002:80

volumes:
  mysql:
  jwt:
  data:
```
