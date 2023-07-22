FROM golang:1.20

WORKDIR /usr/src/app

RUN apt-get update
RUN apt-get install vim -y
# RUN go get "github.com/go-sql-driver/mysql"

ENTRYPOINT go run main.go