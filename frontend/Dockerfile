FROM golang:1.16
WORKDIR /usr/src/app

COPY go.mod ./
RUN go mod download && go mod verify

COPY . .
RUN go build -o app.exe

EXPOSE 8080
CMD ["/usr/src/app/app.exe"]

#To build image
#docker build -t go-frontend .

#To run container
#docker run -d --rm --name frontend -p 8080:8080  go-frontend 

#To stop container
#docker container stop frontend
