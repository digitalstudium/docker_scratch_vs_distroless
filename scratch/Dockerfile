# Build stage
FROM golang:1.21-alpine AS builder
WORKDIR /app
COPY main.go .
ENV GOOS=linux
ENV GOARCH=amd64
RUN go build -ldflags='-w -s -extldflags "-static"' -o myapp main.go

# Final stage with scratch
FROM scratch
COPY --from=builder /app/myapp /
USER 65532
CMD ["/myapp"]
