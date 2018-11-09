FROM golang

RUN mkdir -p /go/src/github.com/divanvisagie/gokit-example-app

ADD . /go/src/github.com/divanvisagie/gokit-example-app

WORKDIR /go/src/github.com/divanvisagie/gokit-example-app/notificator/cmd

RUN go get  -v
RUN go get  github.com/canthefason/go-watcher
RUN go install github.com/canthefason/go-watcher/cmd/watcher

ENTRYPOINT  watcher -run github.com/divanvisagie/gokit-example-app/notificator/cmd  -watch github.com/divanvisagie/gokit-example-app/notificator
