from tensorflow/tensorflow:latest-gpu
ARG DEBIAN_FRONTEND=noninteractive
RUN apt-get update
RUN apt-get update -q
RUN apt-get install dialog apt-utils -y
RUN apt-get -y install python-tk
RUN pip install matplotlib
RUN pip install pillow
RUN pip install scipy
COPY $PWD /app
WORKDIR /app

