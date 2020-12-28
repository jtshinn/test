# base image
FROM hejunpku/tensorflow1.70-cp36:latest

# ADD
ADD requirements.txt /

# MAINTAINER
MAINTAINER xiaoqin

# RUN
RUN pip install -r /requirements.txt

ADD . /main
WORKDIR /main

# EXPOSE
EXPOSE 7070

# CMD
CMD [ "python" , "main.py"]
