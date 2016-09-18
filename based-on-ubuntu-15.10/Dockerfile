FROM ubuntu:15.10

MAINTAINER Ovidiu Dan <contact@ovidiudan.com>

RUN apt-get update && apt-get install -y \
    cython3 \
    gcc \
    ipython3-notebook \
    mc \
    nano \
    python3 \
    python3-numpy \
    python3-pip \
    python3-setuptools \
    python3-scipy \
    vim

RUN locale-gen en_US.UTF-8
ENV LANG en_US.UTF-8 
ENV LC_CTYPE en_US.UTF-8
ENV LC_ALL en_US.UTF-8
RUN easy_install3 --upgrade gensim
RUN pip3 install jupyter
RUN apt-get install -y python3-matplotlib
RUN pip3 install scikit-learn

# docker build . -t gensim
# docker run -it -v <some local directory>:/storage/ -p 9000:9000 gensim /bin/bash
# jupyter notebook --no-browser --port 9000 --ip=*
