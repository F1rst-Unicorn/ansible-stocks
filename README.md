# Stocks Server

Set up a new stocks server and configure it.

## Setup

All relevant variables are listed in the defaults.

### DB Setup

There are two options for DB setup: A local database or a remote one.

In case a local database is used, it is assumed to be up and running and has an
admin user named `stocks_postgresql_admin_user` with `peer` authentication. He
will be used for creation of the database and user for stocks. It configures the
user with password login. For that make sure that `stocks_postgresql_options`
contains a `user` and optionally `password` key. Finally the stocks user must be
able to connect to the db to import schema and inital data.

In case of a remote database, set `stocks_local_database` to `False`. In that
case no DB is configured, only the `stocks.properties` are set up to the
configured values. It is up to you to

* Configure the JDBC driver appropriately

* Create the stocks db and user

* Import the schema and initial data

## References

* [Upstream](https://gitlab.com/veenj/stocks)
