### Distroless

Build:

```bash
docker build -t distroless-image -f distroless/Dockerfile .
```

Test:

```bash
$ docker images --format "{{.Size}}" distroless-image
6.76MB
$ docker run -it distroless-image
Status: 200 OK
Response length: 513 bytes
```

### Scratch

Build:

```bash
docker build -t scratch-image -f scratch/Dockerfile .
```

Test:

```bash
$ docker images --format "{{.Size}}" scratch-image
4.68MB
$ docker run -it scratch-image
Error: Get "https://example.com": tls: failed to verify certificate: x509: certificate signed by unknown authority
```
