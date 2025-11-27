### Distroless

Commands:

```bash
docker build -t distroless-image -f distroless/Dockerfile .
docker images --format "{{.Size}}" distroless-image
docker run -it distroless-image
```

Output:

```bash
Status: 200 OK
Response length: 513 bytes
```

### Scratch

Commands:

```bash
docker build -t scratch-image -f scratch/Dockerfile .
docker images --format "{{.Size}}" scratch-image
docker run -it scratch-image
```

Output:

```bash
Error: Get "https://example.com": tls: failed to verify certificate: x509: certificate signed by unknown authority
```
