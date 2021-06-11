# Docker Main - Worker images

Dockerfile based on bde2020/spark-master image

to build it use:

> docker build . -t spark-main:latest

to run it use:

> docker container run -p 8888:8888 -p 8080:8080 -p 7077:7077 spark-main:latest
