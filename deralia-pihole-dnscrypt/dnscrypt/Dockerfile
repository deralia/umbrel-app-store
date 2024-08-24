# Image to begin with
FROM alpine:3.20.0

# Initial image preparation
RUN apk add --no-cache dnscrypt-proxy

# Copy files into filesystem
COPY dnscrypt-proxy.toml /etc/dnscrypt-proxy/dnscrypt-proxy.toml

# Ports to open
EXPOSE 53/udp 53/tcp

# Start service
CMD ["/usr/bin/dnscrypt-proxy","--config","/etc/dnscrypt-proxy/dnscrypt-proxy.toml"]
