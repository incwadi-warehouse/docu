# Branches

Branches can only be created on the command line.

List all branches and there corresponding id.

```shell
bin/console branch:list
```

Creating a new branch is straightforward. Replace `[NAME]` with your desired name.

```shell
bin/console branch:new [NAME]
```

Delete a branch

- Remove all corresponding books, authors, conditions, formats, genres and tags
- Remove it from MySQL database (table `branch`)
- Remove all related configuration from `conf-api`
- Remove id from env var `BRANCHES` in `search-api`
