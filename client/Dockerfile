FROM debian:bookworm-slim

ENV CERT= \
    KEY= \
    CERTFILE=/cert.pem \
    KEYFILE=/key.pem \
    CACERT= \
    CAPATH= \
    CAFILE= \
    VERIFY=1 \
    PORT=80 \
    DST=127.0.0.1:443

RUN apt-get -y update && \
    apt-get -y upgrade && \
    apt-get -y install socat

COPY start /

ENTRYPOINT ["./start"]
