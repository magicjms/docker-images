FROM python:rc-alpine3.12

LABEL maintainer="jiangms<2368691083@qq.com>"

RUN  echo "Asia/Shanghai" > /etc/timezone

RUN python3 -V
RUN python -V
RUN which pip3
RUN pip3 list
# ubuntu python3 不支持mysqlclient 推荐使用pymysql，解决问题，什么玩意？？？？？
#RUN pip3 install MySQLdb
RUN pip3 install PyMySQL
RUN pip3 install openpyxl
RUN pip3 install requests
RUN pip3 list
