FROM golang:alpine3.15 as build

WORKDIR /usr/src/app

COPY . .

RUN go mod init example/main
RUN go build

FROM scratch

COPY --from=build /usr/src/app/main .

CMD ["./main"]


