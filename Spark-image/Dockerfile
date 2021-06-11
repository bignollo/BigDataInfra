FROM bde2020/spark-master:3.1.1-hadoop3.2

LABEL version="0.1"
LABEL maintainer="bignollo@bignollo.com"
RUN apk add libffi-dev
RUN apk add gcc
RUN apk add python3-dev
RUN apk add py3-zmq
RUN apk add musl-dev
RUN apk add openssl
RUN mkdir /root/.jupyter/
RUN mkdir /root/certs/
COPY jupyter_notebook_config.py /root/.jupyter/
COPY mycert.pem /root/certs/
ENV INIT_DAEMON_STEP=setup_spark
ENV PYSPARK_PYTHON=python3
RUN pip3 install --upgrade pip setuptools wheel notebook findspark
EXPOSE 8888/tcp
EXPOSE 8080/tcp
EXPOSE 7077/tcp
EXPOSE 6066/tcp
CMD jupyter notebook --allow-root
