FROM alpine:3.14.0

LABEL maintainer="jiangms<2368691083@qq.com>"

RUN set -x \
    sed -i 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/g' /etc/apk/repositories \
    && apk add --no-cache build-base \
    && apk add --no-cache zlib zlib-dev \
    && apk add --no-cache python3 \
    && apk add --no-cache busybox-extras \
    && apk add --no-cache python3-dev \
    && python3 -V \
    && mkdir -p /home/data/app

COPY . /home/data/app/
RUN date -R
RUN cd /home/data/app && pwd && ls -alh && tar -xf setuptools-57.0.0.tar.gz && cd setuptools-57.0.0 && ls -alh && python3 setup.py install
RUN cd /home/data/app && pwd && ls -alh && tar -xf pip81-0.0.2.tar.gz && cd pip81-0.0.2 && ls -alh && python3 setup.py install && which pip3