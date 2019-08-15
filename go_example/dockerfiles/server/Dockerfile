FROM golang:1.12

ENV GOPATH /go
WORKDIR /go/src/
COPY go_example go_example
EXPOSE 9995

RUN go get -d -v go_example/server
RUN go install -v go_example/server

CMD ["server"]