ARG GO_VERSION=1.23-alpine

FROM golang:${GO_VERSION} AS builder
WORKDIR /build
COPY go.mod go.sum ./
RUN go mod download
COPY . .
RUN CGO_ENABLED=0 GOOS=linux go build -o /build/main ./cmd/api

FROM alpine:latest
WORKDIR /app
COPY --from=builder /build/main .
EXPOSE 8081
CMD ["./main"]
