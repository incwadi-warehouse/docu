# Setup Manually

## Requirements

- PHP 8.1
- PHP Composer
- NodeJS 14LTS
- Yarn
- MySQL
- SSH Access

## Install Backend

Clone the repository.

```shell
git clone https://github.com/incwadi-warehouse/core.git
```

Change into the created directory.

Create the file `.env.local` and `.env.test.local` with the following content. Please fit it to your needs.

```shell
DATABASE_URL=mysql://DB_USER:DB_PASSWORD@localhost:3306/app
```

[Env Vars](env.md)

Then install the composer dependencies and create the database.

In `prod` run the following command.

```shell
composer install
composer dump-env prod
bin/console doctrine:database:create --if-not-exists
bin/console doctrine:migrations:migrate -n
```

If you are in `dev` run the following commands.

```shell
composer install
bin/console doctrine:database:create --if-not-exists
bin/console doctrine:migrations:migrate -n
bin/console doctrine:fixtures:load -n
```

The fixtures will create an account `admin` with password `password`. This is only for development, you should not use the fixtures in production!

In production you can run `bin/console user:new [USERNAME] [ROLE]`. The first user should have the role `ROLE_ADMIN` for others use `ROLE_USER` or just omit the role.

### Auth

To authenticate your users, you need to generate the SSL keys under `config/jwt/`.

```shell
bin/console lexik:jwt:generate-keypair
```

### Apache Webserver

Point the web root to the `public` dir.

You also need this header for apache.

```apache
SetEnvIf Authorization "(.*)" HTTP_AUTHORIZATION=$1
```

More info on that: <https://github.com/lexik/LexikJWTAuthenticationBundle/blob/master/Resources/doc/index.md#important-note-for-apache-users>

Configure your webserver to redirect all requests to the `index.php` file.

```apache
<IfModule mod_rewrite.c>
  RewriteEngine On
  RewriteCond %{ENV:REDIRECT_STATUS} ^$
  RewriteRule ^index\.php(?:/(.*)|$) %{ENV:BASE}/$1 [R=301,L]
  RewriteCond %{REQUEST_FILENAME} -f
  RewriteRule ^ - [L]
  RewriteRule ^ %{ENV:BASE}/index.php [L]
</IfModule>
```

## Install Frontend

Download the files from the repository.

```shell
git clone https://github.com/incwadi-warehouse/catalog.git
git clone https://github.com/incwadi-warehouse/shop.git
```

The following must be done in **all** of the created directories.

Change into the created directory.

Create the file `.env.local` and overwrite env vars from `.env`, if needed.

[Env Vars](env.md)

Start the build process.

```shell
yarn build
```

The files in `dest/` should be located in your web root.

### Apache Webserver

Configure your webserver to redirect all requests to the `index.html` file.

```apache
<IfModule mod_rewrite.c>
  RewriteEngine On
  RewriteBase /
  RewriteRule ^index\.html$ - [L]
  RewriteCond %{REQUEST_FILENAME} !-f
  RewriteCond %{REQUEST_FILENAME} !-d
  RewriteRule . /index.html [L]
</IfModule>
```
