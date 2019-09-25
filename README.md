<div align="center">
    <a href="#"><img src="logo-linna-96.png" alt="Linna Logo"></a>
</div>

<br/>

<div align="center">
    <a href="#"><img src="logo-db-dumps.png" alt="Linna db Logo"></a>
</div>

<br/>

# About this package
This package contains sql scripts for create the database used from framework, app and auth-mappers.

## SQL scripts

### Mysql
    * `linna_db_mysql.sql` database without data
    * `linna_db_mysql_test.sql` database with data for tests

### Postgresql
    * `linna_db_pgsql.sql` database without data
    * `linna_db_pgsql_test.sql` database with data for tests
    * `linna_db_pgsql_test_scrutinizer.sql` database with data for tests in Scrutinizer CI

# Require
   * Mysql >= 5.5
   * Postgresql >= 10

# Installation

## Composer package
With composer:
```
composer require linna/db-dumps
```

## Dumps to Database
From command prompt, if you don't have a gui tool.

### Mysql
```
mysql -e 'create database linna_db;'
mysql -u root linna_db < vendor/linna/db-dumps/src/linna_db_mysql.sql
```

### Postgresql
```
psql -U postgres -a -f vendor/linna/db-dumps/src/linna_db_pgsql.sql
```