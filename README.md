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

1. Clone the github code from
	https://github.com/shravyanayak/workspace-go.git

2. Write 2 docker files each for Server and Client Application.

3. Install Docker in the machine

4. Setup running and building docker

	$sudo systemctl start docker
	$sudo systemctl enable docker

5. Create Docker Hub account and login to the same in command prompt
6. Build the Server Application

	$ docker build -t shravyanayak/goexample-server -f dockerfiles/server/Dockerfile .

7. Build the Client application

	$ docker build -t shravyanayak/goexample-client -f dockerfiles/client/Dockerfile .

8. Tag Docker images to Docker hub (Server)

	$ docker push shravyanayak/goexample-server

9. Pull Docker images from Docker hub(Server)

	$ docker pull shravyanayak/goexample-server

10. Run Server Application

	$ docker run shravyanayak/goexample-server 

11. Tag Docker images to Docker hub (Client)

	$ docker push shravyanayak/goexample-client

12. Pull Docker images from Docker hub(Client)

	$ docker pull shravyanayak/goexample-client 

13. Run Client Application

	$ docker run shravyanayak/goexample-client


















-










