FROM ubuntu:16.04

RUN apt update && \
    apt install -y \ 
    build-essential \ 
    make

RUN apt install -y libncurses5-dev libgnome2-dev libgnomeui-dev \
libgtk2.0-dev libatk1.0-dev libbonoboui2-dev \
libcairo2-dev libx11-dev libxpm-dev libxt-dev python-dev \
python3-dev ruby-dev lua5.1 lua5.1-dev libperl-dev git

ADD ./ /tmp/
WORKDIR /tmp

RUN tar zxvf vim-8.1.1363.tar.gz
WORKDIR vim-8.1.1363/src/
RUN make
RUN make install

WORKDIR /root
RUN echo set modeline > .vimrc
