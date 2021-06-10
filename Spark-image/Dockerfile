FROM bde2020/spark-master:3.1.1-hadoop3.2

RUN apk add libffi-dev
RUN apk add gcc
RUN apk add python3-dev
RUN apk add py3-zmq
RUN apk add musl-dev
RUN apk add openssl
ENV INIT_DAEMON_STEP=setup_spark
ENV PYSPARK_PYTHON=python3
RUN pip3 install --upgrade pip setuptools wheel notebook
