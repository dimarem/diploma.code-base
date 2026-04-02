ARG GO_VERSION=1.23-alpine

FROM golang:${GO_VERSION} AS builder
WORKDIR /build
COPY go.mod go.sum ./
RUN go mod download
COPY . .
RUN CGO_ENABLED=0 GOOS=linux go build -o /build/main ./cmd/api

FROM alpine:3.19
WORKDIR /app
RUN addgroup -S backend && adduser -S -s /bin/false -G backend backend
COPY --from=builder --chown=backend:backend /build/main ./
USER backend
EXPOSE 8081
CMD ["./main"]
