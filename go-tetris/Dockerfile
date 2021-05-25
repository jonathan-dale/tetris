FROM alpine 
ADD Dockerfile .
RUN apk update &&  apk add --no-cache git make musl-dev go libx11-dev  #### mesa-dev libxcursor-dev libxrandr-dev libxinerama-dev ## (dont need this junk)
ENV GOROOT /usr/lib/go
ENV GOPATH /go
ENV PATH /go/bin:$PATH
RUN mkdir -p ${GOPATH}/src ${GOPATH}/bin

RUN go get github.com/MichaelS11/go-tetris
RUN go install github.com/MichaelS11/go-tetris

