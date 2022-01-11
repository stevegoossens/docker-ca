# docker-ca

A Docker container to generate SSL/TLS certificates

## docker-build

```
docker build -t stevegoossens/docker-ca .
```

## docker run

### All default values

```
docker run -v /tmp/tls:/tls stevegoossens/docker-ca
```

## Override values

```
docker run \
    -v /tmp/tls:/tls \
    -e CA_C=GB \
    -e CA_ST=London \
    -e CA_L=London \
    -e CA_O="British Broadcasting Corporation" \
    -e CA_OU="BBC Dev CA" \
    -e CA_CN="BBC Dev CA - Root" \
    -e CA_EMAIL=dev-ca-admin@bbc.co.uk \
    -e CA_EXPIRE=7305 \
    -e INTERMEDIATE_CA_EXPIRE=3652 \
    stevegoossens/docker-certs
```
