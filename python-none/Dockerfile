FROM ubuntu:bionic

ARG python=Python-3.8.0.tgz
ARG pythondir=Python-3.8.0

WORKDIR /usr/src/app
COPY $python .
RUN tar -xzf $python
RUN rm $python
WORKDIR $pythondir
RUN apt-get update
RUN apt-get install -y build-essential
RUN ./configure
RUN make
# 'make install' raises an error
# RUN make install
