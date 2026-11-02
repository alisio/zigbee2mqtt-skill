# Zigbee adapters

Identify the exact coordinator model, adapter family, firmware and transport before recommending configuration, flashing, or migration. The current configuration example lists `zstack`, `ember`, `deconz`, `zigate`, and `zboss`; verify availability and support in the documentation for the installed version. `ember` is an adapter configuration value; do not substitute a documentation page's title for the value.

For USB adapters, verify a stable device path and access permissions; for network adapters, check the documented transport, reachability and security. Avoid multiple services controlling the same adapter. Flashing and coordinator migration can disrupt or require rebuilding the network: check the specific upstream procedure, back up first, explain recovery limits, and obtain approval.

Sources: [supported adapters](https://www.zigbee2mqtt.io/guide/adapters/), [adapter settings](https://www.zigbee2mqtt.io/guide/configuration/adapter-settings.html), [remote adapters](https://www.zigbee2mqtt.io/advanced/remote-adapter/connect_to_a_remote_adapter.html), [configuration example](https://github.com/Koenkk/zigbee2mqtt/blob/master/data/configuration.example.yaml).
