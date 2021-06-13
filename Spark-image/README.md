# Docker Main - Worker images

Dockerfile based on bde2020/spark-master image

to build it use:

> docker build -t spark-main:latest .

to run it use:

> docker container run -p 8888:8888 -p 8080:8080 -p 7077:7077 spark-main:latest

Once you container is running, you need to get the id with

> docker container ls

and with the ID execute jupyter notebooks

> docker exec CONTAINER_ID jupyter notebook --allow-root

to use pySpark on the notebook, use findspark

> import findspark
> findspark.init('/spark')
> import pyspark

Pending:
* create volume to store notebooks and persist
* add another user to avoid running a root
* Transform master on service.
