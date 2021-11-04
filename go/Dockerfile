FROM golang:latest as builder

WORKDIR /var/www

COPY . .

RUN go build .

FROM scratch

WORKDIR /var/www

COPY --from=builder /var/www/code-education .

ENTRYPOINT ["./code-education"]