# Operations

## Pairing

Check the device-specific pairing instructions first. Open joining temporarily via the frontend or documented MQTT API, put the device in pairing mode, and inspect the interview result. The frontend opens joining for 254 seconds and can close it earlier. Limit the join window and close it after use. Distinguish a device that did not join from one whose interview failed.

## Groups, scenes and binding

Use the upstream guides to select group membership, configure scenes, or bind compatible endpoints. Zigbee binding and MQTT automation are different mechanisms. Verify device and endpoint capabilities before changing them; test the resulting behavior.

## OTA updates

Check model, firmware, supported update path, power supply, and release-specific instructions. Obtain approval before updating; a failed firmware update can make a device unavailable. Monitor progress and verify operation afterward.

## Backup and coordinator migration

Before changes, protect a consistent backup of the data directory and any coordinator backup; these can contain network keys. Record the current coordinator, firmware, network parameters and version. Check the official migration procedure and backup compatibility for both adapters; do not assume copying configuration alone preserves coordinator state. Keep the original coordinator and backup for rollback and avoid running two coordinators with the same network identity simultaneously. Migration may require re-pairing.

Sources: [pairing](https://www.zigbee2mqtt.io/guide/usage/pairing_devices.html), [groups](https://www.zigbee2mqtt.io/guide/usage/groups.html), [scenes](https://www.zigbee2mqtt.io/guide/usage/scenes.html), [binding](https://www.zigbee2mqtt.io/guide/usage/binding.html), [OTA](https://www.zigbee2mqtt.io/guide/usage/ota_updates.html), [adapters and migration](https://www.zigbee2mqtt.io/guide/adapters/).
