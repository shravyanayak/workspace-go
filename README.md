# workspace-go

There are 2 steps to run client-server gRPC program:

Running Locally

1. Download goLang latest version 

$ wget https://dl.google.com/go/go1.12.7.linux-amd64.tar.gz

Extract the above folder and install it.

2. Set up Go Environment

-GOROOT is the location of the installed packages.

$ export GOROOT=/go

-GOPATH is the location of work directory

$ export GOPATH=$HOME/Documents/go/go_example

-Set the PATH variable to access go binary.

$ export PATH=$GOROOT/bin:$PATH

3. To get started with gRPC, we need to install below things.

- protocol buffer compiler

$ sudo apt install protobuf-compiler

-install below packages

$ go get -u google.golang.org/grpc   
$ go get -u github.com/golang/protobuf/protoc-gen-go
$ go get -u github.com/gogo/protobuf/proto
$ go get -u github.com/gogo/protobuf/protoc-gen-go
$ go get -u github.com/gogo/protobuf/gogoproto

4. Connecting server with client using gRPC

$ protoc --gogo_out=. message.proto (inside protobuf directory)

5. Run server

$ go run main.go

6. Run client

$ go run main.go



-









