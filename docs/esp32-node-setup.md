# ESP32 Node Setup

This project uses ESPresense firmware on ESP32 nodes.

## Basic Idea

Each ESP32 becomes a BLE scanner for one room.

Example node names:

```text
living-room
bedroom
office
hallway
kitchen
```

## Flashing

Use the official ESPresense flashing method from the ESPresense documentation.

After flashing, configure:

- Wi-Fi SSID
- Wi-Fi password
- MQTT host
- MQTT port
- room/node name
- optional MQTT username/password

## MQTT Host

Use the IP address of your Docker server.

Example:

```text
192.168.1.50
```

## Recommended Placement

Place ESP32 nodes:

- one per room
- away from metal
- powered permanently
- not inside cabinets
- at similar height where possible

## Accuracy Tips

- Use more nodes for better room accuracy.
- Keep room names consistent.
- Avoid moving ESP32 nodes after calibration.
- BLE RSSI can be noisy; do not expect centimeter-level accuracy.
