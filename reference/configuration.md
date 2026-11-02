# Configuration and integration

- Configuration is `configuration.yaml` in the Zigbee2MQTT data directory, which must be writable by the process. `ZIGBEE2MQTT_DATA` can select a different data directory. Stop Zigbee2MQTT before editing the file manually; otherwise changes can be overwritten.
- Environment variables prefixed `ZIGBEE2MQTT_CONFIG_` can override settings; for example, `ZIGBEE2MQTT_CONFIG_MQTT_BASE_TOPIC` overrides `mqtt.base_topic`. Inspect the actual deployment before changing either source.
- The current upstream example uses configuration `version: 5`, `mqtt.server`, `mqtt.base_topic`, `homeassistant.enabled`, `frontend.enabled`, and, when needed, `serial.port` and `serial.adapter`. This is a configuration migration version, not the application version. Verify the schema and example for the installed release.
- Zigbee2MQTT can change settings via its frontend or `bridge/request/options`; some changes need a restart. Do not assume the broker is reachable at `localhost` from a container: check the actual network topology.
- Home Assistant discovery requires the MQTT integration and an accessible broker; check discovery settings on both sides and inspect MQTT messages before diagnosing entities.
- Keep broker credentials and Zigbee network keys confidential; redact logs and examples. Avoid exposing the frontend or broker to untrusted networks.

Sources: [configuration](https://www.zigbee2mqtt.io/guide/configuration/), [MQTT](https://www.zigbee2mqtt.io/guide/configuration/mqtt.html), [Home Assistant](https://www.zigbee2mqtt.io/guide/configuration/homeassistant.html), [example configuration](https://github.com/Koenkk/zigbee2mqtt/blob/master/data/configuration.example.yaml), [schema](https://github.com/Koenkk/zigbee2mqtt/blob/master/lib/util/settings.schema.json).
