FROM ubuntu

MAINTAINER vikas.bodke@neosoftmail.com


RUN apt-get update
RUN apt-get install -y python python3-pip
RUN pip3 install flask

RUN apt-get clean && apt-get update && apt-get install -y locales
RUN locale-gen en_US.UTF-8
ENV LANG en_US.UTF-8
ENV LANGUAGE en_US:en
ENV LC_ALL en_US.UTF-8

COPY app.py /opt/app.py

ENTRYPOINT FLASK_APP=app.py flask run --host=0.0.0.0



