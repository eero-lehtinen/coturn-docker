# Coturn Docker

Coturn running in STUN-only mode via Docker.

## Build

```sh
docker build -t coturn .
```

## Run

```sh
docker run -d --network host --name coturn coturn
```

The `--network host` flag is used so the server can see clients' real IP addresses and correctly respond to STUN binding requests. Port 3478/udp is used by default.
