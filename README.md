# Sample Liquibase Docker Project

Welcome to this project that demonstrates how to use Liquibase, PostgreSQL and Docker containers together to manage database schema changes. If you're not familiar with it, Liquibase is an open-source tool for database schema management that allows developers to version their database schema and apply changes to it over time. Sooooorta `sqlpackage` for SQL Server.

In this project, we will use Docker containers to set up a PostgreSQL database and run Liquibase to manage the database schema updates. We will demonstrate how to create a database migration script, apply it to the database and roll back changes if necessary.

To get started, run the code below.

```bash
# clone repo and change directories
git clone https://www.github.com/potatoqualitee/liquibase
cd liquibase

# start the containers which creates some tables and makes some changes
docker compose up -d

# see the results
docker exec db psql -U postgres -c "select * from customers;"

# tear it down
docker compose down --volumes
```

All scripts inside /scripts folder will be executed on target database

Check out the [Liquibase toolbox](https://github.com/liquibase/liquibase-toolbox) for more scripts.