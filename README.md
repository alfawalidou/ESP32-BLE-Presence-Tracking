# ESP32 BLE Presence Tracking

Bluetooth/BLE room presence tracking project using ESP32 nodes, MQTT, Docker, Mosquitto, Node-RED, and optional ESPresense Companion.

This project is for tracking BLE devices such as:

- phones
- watches
- BLE tags
- smart bands
- key trackers
- pet tags
- asset trackers

It is different from mmWave presence detection. BLE tracking can identify *which device/person* is nearby, while mmWave detects if *someone* is physically present.

---

## Project Architecture

```text
BLE devices
    ↓
ESP32 ESPresense nodes
    ↓ MQTT
Mosquitto broker in Docker
    ↓
Node-RED dashboard / automations
    ↓
Optional ESPresense Companion
```

---

## Features

- Room-level BLE presence tracking
- MQTT-based architecture
- Docker-ready local server stack
- Optional ESPresense Companion container
- Node-RED dashboard starter flow
- Mosquitto configuration
- Documentation for setup, devices, MQTT, and troubleshooting

---

## Required Hardware

| Item | Purpose |
|---|---|
| ESP32 board | BLE scanning node |
| USB power supply | Powers each ESP32 |
| BLE device | Phone, watch, tag, beacon |
| Docker server | Runs MQTT/dashboard stack |

Recommended ESP32 boards:

- ESP32 DevKit V1
- ESP32-WROOM-32
- M5Stack Atom Lite
- ESP32-C3 boards
- ESP32-S3 boards

---

## Required Software

- Docker
- Docker Compose
- ESPresense firmware on ESP32 nodes
- Mosquitto MQTT broker
- Optional Node-RED
- Optional ESPresense Companion

---

## Quick Start

1. Clone this repository.
2. Edit `docker/.env`.
3. Start the Docker stack:

```bash
cd docker
docker compose up -d
```

4. Open services:

```text
Node-RED:              http://SERVER_IP:1880
ESPresense Companion: http://SERVER_IP:8267
MQTT broker:           SERVER_IP:1883
```

5. Flash ESPresense firmware to your ESP32 nodes.
6. Configure each ESP32 node with:
   - Wi-Fi SSID/password
   - MQTT host
   - MQTT username/password if enabled
   - room name
7. Watch MQTT messages in Node-RED or ESPresense Companion.

---

## Documentation

- [Docker Setup](docs/docker-setup.md)
- [ESP32 Node Setup](docs/esp32-node-setup.md)
- [MQTT Topics](docs/mqtt-topics.md)
- [Dashboard Guide](docs/dashboard.md)
- [Troubleshooting](docs/troubleshooting.md)
- [Privacy Notes](docs/privacy.md)

---

## Repository Structure

```text
ESP32-BLE-Presence-Tracking/
├── README.md
├── LICENSE
├── .gitignore
├── docker/
│   ├── docker-compose.yml
│   ├── .env.example
│   ├── mosquitto/
│   │   └── config/
│   │       └── mosquitto.conf
│   └── nodered/
│       └── flows.json
├── docs/
│   ├── docker-setup.md
│   ├── esp32-node-setup.md
│   ├── mqtt-topics.md
│   ├── dashboard.md
│   ├── privacy.md
│   ├── troubleshooting.md
│   └── images/
│       └── architecture.png
└── examples/
    └── mqtt-test-commands.md
```

---

## GitHub Topics

Recommended topics:

```text
esp32
ble
bluetooth
presence-detection
mqtt
mosquitto
nodered
docker
espresense
home-automation
indoor-positioning
iot
```

---

## Notes

This repository does not replace the official ESPresense firmware. It provides a clean project structure, Docker stack, documentation, and dashboard starter files to build your own BLE presence tracking system.

Official ESPresense project:

https://github.com/ESPresense/ESPresense

Official ESPresense documentation:

https://espresense.com/
