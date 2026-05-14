# Troubleshooting

## No MQTT Messages

Check:

- ESP32 is connected to Wi-Fi
- MQTT host IP is correct
- Docker stack is running
- Mosquitto port 1883 is open
- ESPresense node room name is configured

Run:

```bash
docker compose logs -f mosquitto
```

## Node-RED Shows Nothing

Check the MQTT broker config in Node-RED.

The included flow uses broker hostname:

```text
mosquitto
```

This works inside Docker Compose.

## Companion Does Not See Nodes

Check:

- Companion container is running
- MQTT settings inside Companion
- ESP32 nodes are publishing to the same broker
- Ports 8267 and 8268 are open

## Poor Room Accuracy

BLE RSSI is noisy.

Improve by:

- adding more ESP32 nodes
- placing nodes away from metal
- avoiding USB power banks that sleep
- keeping nodes in fixed positions
- tuning/calibrating devices
