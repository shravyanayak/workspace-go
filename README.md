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


Building and Running using Docker container images:

Clone the github code from
	https://github.com/shravyanayak/workspace-go.git

Write 2 docker files each for Server and Client Application.

Install Docker in the machine

Setup running and building docker

$sudo systemctl start docker
$sudo systemctl enable docker

Create Docker Hub account and login to the same in command prompt
Build the Server Application

$ docker build -t <docker-username>/goexample-server -f dockerfiles/server/Dockerfile .

Build the Client application

$ docker build -t <docker-username>/goexample-client -f dockerfiles/client/Dockerfile .

Tag Docker images to Docker hub (Server)

$ docker push <docker-username>/goexample-server

Pull Docker images from Docker hub(Server)

$ docker pull <docker-username>/goexample-server

Run Server Application

$ docker run <docker-username>/goexample-server 

Tag Docker images to Docker hub (Client)

$ docker push <docker-username>/goexample-client

Pull Docker images from Docker hub(Client)

$ docker pull <docker-username>/goexample-client 

Run Client Application

$ docker run <docker-username>/goexample-client


















-










