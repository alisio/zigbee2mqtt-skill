# Troubleshooting

1. Capture the installed Zigbee2MQTT version, deployment method, relevant redacted logs, adapter model and firmware, and exact symptom. Establish when the issue began and what changed.
2. **Startup failure:** inspect service logs, configuration validity, serial adapter path, adapter type, permissions, exclusive access to the coordinator, and broker connection independently. Verify USB passthrough if containerized.
3. **Pairing failure:** verify the supported device page and pairing procedure, join window, interview messages, distance, radio interference, and router availability. Avoid resetting an existing network as a diagnostic shortcut.
4. **Unstable or missing devices:** distinguish a sleeping battery device from a broken route, broker disconnection, or stale integration state. Check network topology, interference, adapter placement, and device power before changing channel or firmware.
5. **Missing Home Assistant entity:** check Zigbee2MQTT device state, MQTT traffic, discovery configuration, and Home Assistant's MQTT integration separately.
6. Record the finding and test one reversible change at a time; verify the result and explain rollback before disruptive steps.

Sources: [troubleshooting](https://www.zigbee2mqtt.io/guide/usage/troubleshooting.html), [startup failures](https://www.zigbee2mqtt.io/guide/installation/20_zigbee2mqtt-fails-to-start_crashes-runtime.html), [FAQ](https://www.zigbee2mqtt.io/guide/faq/), [network stability](https://www.zigbee2mqtt.io/advanced/zigbee/02_improve_network_range_and_stability.html).
