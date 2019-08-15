FROM golang:1.12

ENV GOPATH /go
WORKDIR /go/src/
COPY go_example go_example

RUN go get -d -v go_example/client
RUN go install -v go_example/client

CMD ["client"]