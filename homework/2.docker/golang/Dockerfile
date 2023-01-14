FROM golang:1.19 as builder

WORKDIR /app

COPY . /app

RUN CGO_ENABLED=0 GOOS=linux GOARCH=amd64 go build -o server .

FROM alpine	

COPY --from=builder /app/server /

EXPOSE 8080

CMD ["/server"]

