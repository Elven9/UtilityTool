# Protobuf Builder for Golang

The tool helps to compile target `.proto` file to golang codes to a certain directory without installing compiler on your own laptop.

## Current Status

- Golang Version: 1.14
- Protocol Buffer Version: [protobuf-cpp-3.11.4](https://github.com/protocolbuffers/protobuf/releases/download/v3.11.4/protobuf-cpp-3.11.4.zip)

## Usage

```shell
#/bin/zsh
# Build The Image
docker build -t elven9/protobuf-builder-for-golang .

# Start A Container and Bind The Source Codes to Container
docker run --rm -it --mount type=bind,source=$(pwd),target=/go/protobuf-src elven9/protobuf-builder-for-go
```