# MQTT Test Commands

Subscribe to all ESPresense topics:

```bash
docker exec -it ble-presence-mosquitto mosquitto_sub -h localhost -t 'espresense/#' -v
```

Publish a test message:

```bash
docker exec -it ble-presence-mosquitto mosquitto_pub -h localhost -t 'espresense/test' -m 'hello'
```

Watch Docker logs:

```bash
cd docker
docker compose logs -f
```
