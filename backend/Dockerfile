FROM golang:latest

WORKDIR /go/src
COPY . .

RUN apt-get update && \
    apt-get install git

RUN go get -u github.com/cosmtrek/air && \
    go build -o /go/bin/air github.com/cosmtrek/air

RUN go mod tidy

EXPOSE 8000

CMD ["go", "run", "main.go"]
