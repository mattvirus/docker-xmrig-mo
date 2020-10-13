FROM ubuntu:xenial

RUN apt-get -y update && \
    apt-get -y upgrade

RUN apt-get install -y git build-essential cmake make libuv1-dev libmicrohttpd-dev gcc g++ \
        automake autoconf pkg-config libcurl4-openssl-dev libjansson-dev libssl-dev libgmp-dev 
    
RUN git clone https://github.com/MoneroOcean/xmrig && \
    cd xmrig && mkdir build && cd build && \
    cmake .. && \
    make && \
    mv xmrig /usr/local/bin
