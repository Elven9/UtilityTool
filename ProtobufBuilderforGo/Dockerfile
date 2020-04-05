# Base Image from Golang Debian Version.
FROM golang:1.14.1-buster

# Install C++ Version's Protobuf Compiler
RUN apt-get update && \
    yes | apt-get install autoconf automake libtool curl make g++ unzip && \
    wget -O cpp.zip https://github.com/protocolbuffers/protobuf/releases/download/v3.11.4/protobuf-cpp-3.11.4.zip && \
    unzip cpp.zip && rm cpp.zip && \
    cd protobuf-3.11.4 && \
    ./configure && \
    make && \
    make check && \
    make install && \
    ldconfig && \
    cd .. && rm -rf protobuf-3.11.4

# Install Go Plugin
RUN go get -u github.com/golang/protobuf/protoc-gen-go
