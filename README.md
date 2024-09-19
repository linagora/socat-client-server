# Simple SSL bridge

Client example:
```shell
$ docker run --rm  -p 3000:3000 \
    -e PORT=3000 \
    -e DST=socat-server:4000 \
    -v pathToClientCert.pem:/cert.pem \
    -v pathToKey.pam:/key.pem \
    yadd/socat-client
```

Server example
```shell
$ docker run --rm  -p 4000:4000 \
    -e PORT=4000 \
    -e DST=hidden-server:80 \
    -v pathToClientCert.pem:/cert.pem \
    -v pathToKey.pam:/key.pem
```
