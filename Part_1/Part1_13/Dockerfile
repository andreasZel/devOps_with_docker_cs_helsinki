FROM ubuntu:22.04

EXPOSE 8080

WORKDIR /usr/src/app

RUN apt-get update && apt-get -y install curl wget tar

RUN wget https://go.dev/dl/go1.16.15.linux-amd64.tar.gz
RUN tar -C . -xzf go1.16.15.linux-amd64.tar.gz

ENV PATH="$PATH:/usr/src/app/go/bin"

COPY . .

RUN go build

ENTRYPOINT ["./server"]