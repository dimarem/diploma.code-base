ARG GO_VERSION=1.23-alpine

FROM golang:${GO_VERSION} AS builder
WORKDIR /build
RUN adduser -D -u 10001 appuser
COPY go.mod go.sum ./
RUN go mod download
COPY . .
RUN CGO_ENABLED=0 GOOS=linux go build -o /build/main ./cmd/api

FROM alpine:3.19
WORKDIR /app
COPY --from=builder /build/main .
USER appuser
EXPOSE 8081
CMD ["./main"]
