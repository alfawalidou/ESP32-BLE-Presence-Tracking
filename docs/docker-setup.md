# Docker Setup

This Docker stack includes:

- Mosquitto MQTT broker
- Node-RED dashboard/automation engine
- ESPresense Companion

## Start

```bash
cd docker
cp .env.example .env
docker compose up -d
```

## Open Services

```text
Node-RED:              http://SERVER_IP:1880
ESPresense Companion: http://SERVER_IP:8267
MQTT broker:           SERVER_IP:1883
```

## Stop

```bash
docker compose down
```

## View Logs

```bash
docker compose logs -f
```

## MQTT Security

The starter config allows anonymous MQTT for simple local testing.

For a permanent setup, create MQTT usernames/passwords and disable anonymous access.
