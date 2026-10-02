# Contributing

Contributions are welcome when they improve reliability, documentation, or interoperability.

## Before submitting a change

- Keep firmware, MQTT, Docker, and Node-RED changes focused.
- Never commit Wi-Fi credentials, MQTT passwords, API keys, tokens, or device identifiers.
- Document any new MQTT topics or environment variables.
- Validate Docker changes with `docker compose config` when possible.
- Describe the ESP32 board and firmware version used for hardware-related changes.

## Pull requests

Explain what changed, why it is useful, and how it was tested. For hardware-specific changes, include enough detail for another user to reproduce the setup.