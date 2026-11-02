---
name: zigbee2mqtt
description: Use when installing, configuring, operating, integrating, or troubleshooting Zigbee2MQTT, MQTT, Zigbee adapters, devices, pairing, OTA updates, or Home Assistant discovery.
---

# Zigbee2MQTT

Use the installed version's official documentation and device-specific exposes as the authority. This reference targets Zigbee2MQTT 2.x; check the installed version and matching release before applying version-dependent changes. Current upstream documentation and schema can change.

## Workflow

1. Identify the version, deployment method, coordinator and firmware, MQTT broker, and affected device model. Ask for missing details when they change the answer.
2. Inspect configuration and logs without exposing passwords, network keys, or tokens. Read the relevant reference below and verify version-specific details against the linked upstream source.
3. Separate Zigbee radio, Zigbee2MQTT, MQTT, and integration failures. Prefer reversible diagnostics; ask before modifying live settings, joining, removing, updating, resetting, or migrating devices.
4. Explain the proposed action, its risks and rollback, and verify the observed result. Verify support against the relevant upstream device or adapter page.

| Task | Reference |
| --- | --- |
| Configuration, MQTT, Home Assistant | [Configuration](reference/configuration.md) |
| MQTT topics, commands, bridge API | [MQTT topics](reference/mqtt-topics.md) |
| Pairing, groups, OTA, migration | [Operations](reference/operations.md) |
| Startup, pairing, stability, logging | [Troubleshooting](reference/troubleshooting.md) |
| Coordinator selection and firmware | [Adapters](reference/adapters.md) |

## Common mistakes

- Editing `configuration.yaml` while Zigbee2MQTT is running: stop it first or use the documented runtime API; edits can be overwritten.
- Assuming the MQTT base topic is always `zigbee2mqtt`, or that every device supports the same properties: check the configuration and device exposes.
- Treating an MQTT response as proof of physical device state, or a device's absence from Home Assistant as proof it failed to join Zigbee.
- Changing the network key, PAN identifiers, radio firmware, or channel without a protected backup and a version- and adapter-specific recovery plan.
- Leaving pairing enabled longer than necessary or exposing the broker and frontend without access controls.

Sources: [official documentation](https://www.zigbee2mqtt.io/), [documentation repository](https://github.com/Koenkk/zigbee2mqtt.io), [application repository](https://github.com/Koenkk/zigbee2mqtt).
