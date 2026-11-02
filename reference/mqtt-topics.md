# MQTT topics and messages

The examples use the default base topic `zigbee2mqtt`; replace it with the configured `mqtt.base_topic`. Device names can contain `/`. Consult the device's **Exposes** page before assuming a property is supported.

| Topic | Purpose |
| --- | --- |
| `zigbee2mqtt/FRIENDLY_NAME` | Published device or group state |
| `zigbee2mqtt/FRIENDLY_NAME/set` | Set supported properties using a JSON object |
| `zigbee2mqtt/FRIENDLY_NAME/get` | Request supported properties |
| `zigbee2mqtt/FRIENDLY_NAME/availability` | Availability when enabled |
| `zigbee2mqtt/bridge/request/ACTION` | Bridge API request |
| `zigbee2mqtt/bridge/response/ACTION` | Corresponding response with `status` and `data`; failures also include `error` |

Example for a light exposing `state`: subscribe to `zigbee2mqtt/living_room`, then publish `{"state":"ON"}` to `zigbee2mqtt/living_room/set`. To request its state, publish `{"state":""}` to `zigbee2mqtt/living_room/get`; `/get` support depends on the device's exposes. A command response or cached state alone does not prove the light physically changed.

Permit joining temporarily: publish `{"time":60}` to `zigbee2mqtt/bridge/request/permit_join`; close it with `{"time":0}` on the same topic. Time is in seconds. The documented maximum example uses 254 seconds. Subscribe to `zigbee2mqtt/bridge/response/permit_join` and check `status`; optionally add a `transaction` to match requests and responses. Confirm the request format for the installed release.

Sources: [MQTT topics and bridge API](https://www.zigbee2mqtt.io/guide/usage/mqtt_topics_and_messages.html), [exposes](https://www.zigbee2mqtt.io/guide/usage/exposes.html), [supported devices](https://www.zigbee2mqtt.io/supported-devices/).
