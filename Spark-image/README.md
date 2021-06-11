# Docker Main - Worker images

Dockerfile based on bde2020/spark-master image

to build it use:

> docker build -t spark-main:latest .

to run it use:

> docker container run -p 8888:8888 -p 8080:8080 -p 7077:7077 spark-main:latest

then,  from the logs you can get the url to connect to jupyter notebooks

in order to execute spark you need to use findspark:

> import findspark
> findspark.init('/spark')
> import pyspark

Pending:
* create volume to store notebooks and persist
* add another user to avoid running a root
