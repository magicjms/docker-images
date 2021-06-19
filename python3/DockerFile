FROM alpine:3.14.0

LABEL maintainer="jiangms<2368691083@qq.com>"

RUN set -x \
    && apk add build-base zlib-dev gcc

RUN wget https://www.python.org/ftp/python/3.9.5/Python-3.9.5.tgz && tar -xf Python-3.9.5.tgz && cd Python-3.9.5 && ls -alh
RUN cd Python-3.9.5 && ls -alh && ./configure --enable-optimizations --with-ensurepip=install && make -j 8 && make altinstall
RUN python3 -V

# RUN set -x \
#     sed -i 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/g' /etc/apk/repositories \
#     && apk add --no-cache build-base \
#     && apk add --no-cache zlib zlib-dev \
#     && apk add --no-cache python3 \
#     && apk add --no-cache busybox-extras \
#     && apk add --no-cache python3-dev \
#     && python3 -V \
#     && mkdir -p /home/data/app

# COPY . /home/data/app/
# RUN date -R
# RUN cd /home/data/app && pwd && ls -alh && tar -xf setuptools-57.0.0.tar.gz && cd setuptools-57.0.0 && ls -alh && python3 setup.py install
# RUN cd /home/data/app && pwd && ls -alh && tar -xf pip81-0.0.2.tar.gz && cd pip81-0.0.2 && ls -alh && python3 setup.py install && which pip3