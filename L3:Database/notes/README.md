# PostgreSQL

PostgreSQL, or Postgres, is a relational database management system that provides an implementation of the SQL querying language. It’s standards-compliant and has many advanced features like reliable transactions and concurrency without read locks.
Its an open source database and very popular in the startup world.

For any doubts first try to find out solution in the official documentation. Then go to stackoverflow or google.

* Creating new user/role
``` sql
CREATE ROLE app_user WITH LOGIN PASSWORD 'app_password';

CREATE USER ipl_data WITH PASSWORD 'user123';
```

* Alter the permissions 
``` sql
ALTER ROLE app_user CREATEDB;
```

* See user list
``` psql
\du
```

* Exit the current user
``` psql
\q
```

* Login to other user$ psql postgres -U app_user
* Create database
``` sql
CREATE DATABASE mydb WITH OWNER my_user;
```
* Delete database
``` sql
DROP DATABASE mydb;
```
* Connecting to the database
``` sh
$ psql database_name
```

In above case it will take the default value of all other parameters
``` sh
$ psql -h localhost -p 5432 -U roleName database_name
```

* Switch database with current user
``` sql
\c data_base
```

* Create table 
``` sql
CREATE TABLE teble_name(
    columns_name data_type contraints if any
);
```

* login with user
``` sh
$ psql -U ipl_data ipl
```

* Running sql script through a file\
    * using CLI
``` sh
$ sudo -U potgres psql -f filename
or 
$ psql -U user database -f filename
```
* using psql

``` sql
\i filename
```

* copy data between file and table
``` sql
-- set path variable of the file
\set deliveries_path `pwd` '/dataset/deliveries.csv'

COPY deliveries
FROM :'deliveries_path'
DELIMITER ','
CSV HEADER;
```
