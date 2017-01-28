# Create, alter, delete and list roles in PostgreSQL

To create a new role use following command:

```
CREATE ROLE user WITH LOGIN ENCRYPTED PASSWORD 'password';
```

To change the role(e.g. give new permissions) run:

```
ALTER ROLE user WITH CREATEDB;
```

To list all roles:

```
\du
```

This will give you following output:

```
 Role name |                   Attributes                   | Member of
-----------+------------------------------------------------+-----------
 phil      | Superuser, Create role, Create DB, Replication | {}
 user      | Create DB                                      | {}
```


To delete a role run:

```
DROP ROLE user;
```

Read more here: https://www.postgresql.org/docs/8.1/static/sql-createrole.html
