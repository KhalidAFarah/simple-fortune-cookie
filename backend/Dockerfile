FROM golang:1.16
WORKDIR /usr/src/app

COPY go.mod ./
RUN go mod download && go get github.com/gomodule/redigo@v1.8.5 && go mod verify

COPY . .
RUN go build -o app.exe

EXPOSE 9000
EXPOSE 6379

CMD ["/usr/src/app/app.exe"]

#To build image
#docker build -t go-backend .

#To run container
#docker run -d --rm --name backend -p 9000:9000  go-backend

#To stop container
#docker container stop backend
