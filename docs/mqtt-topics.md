# MQTT Topics

ESPresense publishes BLE detection data to MQTT.

Common patterns include:

```text
espresense/rooms/ROOM_NAME
espresense/devices/DEVICE_ID
```

Exact topics can depend on ESPresense version and configuration.

## Test MQTT

From Docker server:

```bash
docker exec -it ble-presence-mosquitto mosquitto_sub -h localhost -t 'espresense/#' -v
```

You should see messages when BLE devices are detected.

## Node-RED

The included Node-RED starter flow subscribes to:

```text
espresense/#
```

and prints messages to the debug sidebar.
