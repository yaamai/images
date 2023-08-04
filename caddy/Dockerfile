FROM caddy:2.7.2-builder-alpine as builder
RUN xcaddy build \
    --with github.com/caddy-dns/cloudflare \
    --with github.com/greenpau/caddy-security

FROM caddy:2.7.2-alpine
COPY --from=builder /usr/bin/caddy /usr/bin/caddy

