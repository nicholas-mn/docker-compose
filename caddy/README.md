
# Setup

Network is set to `external: true`, so the `caddy` network needs to be created seperately before running:

`$ docker network create caddy`

My reasoning for doing this, is so the network don't disappear if I decide to do a `docker compose down` for whatever reason.

# Logging

If you want to add logging in Caddyfile, use following snippet under a domain declaration:

    log {
        output file /var/log/caddy/example.com-access.log
        format json
    }
