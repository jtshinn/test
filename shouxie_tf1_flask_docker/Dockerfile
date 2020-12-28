# base image
FROM ubuntu:latest
# ADD
ADD hello.sh /hello.sh
# MAINTAINER
MAINTAINER xiaoqin
# RUN
RUN chmod +x /hello.sh
RUN ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
# build
RUN apt -y  update --fix-missing && apt -y full-upgrade --fix-missing \
&& apt -y install --fix-missing build-essential \
&& apt -y install --fix-missing -y make libssl-dev zlib1g-dev libbz2-dev libpcre3 libpcre3-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev libperl-dev libncursesw5-dev xz-utils tk-dev zlib1g libffi-dev liblzma-dev screen git vim nano openssl gcc \
# py3.8
RUN mkdir /usr/local/python3 && cd /usr/local/python3 \
&& wget https://www.python.org/ftp/python/3.8.7/Python-3.8.7.tgz \
&& tar xf Python-3.8.7.tgz && cd Python-3.8.7 \
&& ./configure  --enable-optimizations && make && make install \
&& pip3 install --upgrade pip
#nginx
RUN mkdir /usr/local/nginx && cd /usr/local/nginx && wget http://nginx.org/download/nginx-1.18.0.tar.gz \
&& tar -zxvf nginx-1.18.0.tar.gz && cd nginx-1.18.0 && ./configure --with-http_ssl_module --with-http_v2_module \
&& make && make install \
# CMD
CMD ["bin/bash","-c","/hello.sh"]
# EXPOSE
EXPOSE 3000 80 443 22 7080 8080 7070 7060 7050 7040 7030 7020 7010 7000 8000
