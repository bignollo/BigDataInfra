[![Gitter chat](https://badges.gitter.im/gitterHQ/gitter.png)](https://gitter.im/big-data-europe/Lobby)

# docker-hive

Container for Apache Hive 3.1.2,  based on https://github.com/big-data-europe/docker-hadoop so check there for Hadoop configurations.
This deploys Hive and starts a hiveserver2 on port 10000.
Metastore is running with a connection to postgresql database.
The hive configuration is performed with HIVE_SITE_CONF_ variables (see hadoop-hive.env for an example).

The container is an update from Ivan Ermilov's [@earthquakesan](https://github.com/earthquakesan) version https://hub.docker.com/r/bde2020/hive/

to build the container simply use:

> docker build .

and then you can use the docker compose on the top level of the repo.

Also, using the top level docker-compose file you can just pull it from my repo.
