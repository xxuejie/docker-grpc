# Build
FROM golang:1.8-alpine3.6 as builder
MAINTAINER Xuejie Xiao <xxuejie@gmail.com>
RUN apk --no-cache add git
RUN go get google.golang.org/grpc
RUN go get github.com/golang/protobuf/protoc-gen-go

# Run
FROM alpine:3.6
MAINTAINER Xuejie Xiao <xxuejie@gmail.com>
RUN apk --no-cache add protobuf
COPY --from=builder /go/bin/protoc-gen-go /bin/protoc-gen-go
