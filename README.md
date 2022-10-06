```
docker run \
  --detach \
  --name caddy \
  --hostname caddy \
  --restart always \
  --publish 80:80/tcp \
  --publish 443:443/tcp \
  --publish 80:80/udp \
  --publish 443:443/udp \
  --volume ~/caddy/Caddyfile:/etc/caddy/Caddyfile \
  --volume ~/caddy/data:/data \
  --env CLOUDFLARE_API_TOKEN="******************" \
  --env TZ="UTC" \
  ghcr.io/oscarhult/caddy
```
