
FROM golang:1.20.3

WORKDIR /app

COPY go.mod go.sum ./

RUN go mod download && go mod verify

COPY . . 

RUN go build -o ./bin/product *.go

EXPOSE 9090

CMD [ "./bin/product" ]


