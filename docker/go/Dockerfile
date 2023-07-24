FROM golang:1.20

WORKDIR /usr/src/app

RUN apt-get update \
apt-get install vim -y \
curl -L https://packagecloud.io/golang-migrate/migrate/gpgkey | apt-key add - \
echo "deb https://packagecloud.io/golang-migrate/migrate/ubuntu/ $(lsb_release -sc) main" > /etc/apt/sources.list.d/migrate.list \
apt-get update \
apt-get install -y migrate \
migrate -help \
migrate -source file://migrations -database postgres://localhost:5432/database up 2

# RUN go get "github.com/go-sql-driver/mysql"

ENTRYPOINT go run main.go