# Zigbee2MQTT skill

An agent skill for operating and integrating Zigbee2MQTT. It covers configuration, MQTT, pairing, adapters, updates, and troubleshooting. The reference targets Zigbee2MQTT 2.x; consult the linked upstream documentation for the installed version.

## Installation

Copy `SKILL.md` and `reference/` into a directory named `zigbee2mqtt` under your harness's skills directory. The skill and its references must remain together. The following are common user-level locations; consult your harness documentation for the location supported by your version:

| Harness | Skill directory |
| --- | --- |
| OpenCode | `~/.config/opencode/skills/zigbee2mqtt` |
| Claude Code | `~/.claude/skills/zigbee2mqtt` |
| Codex | `~/.agents/skills/zigbee2mqtt` |

For example, from the root of this repository, to install for OpenCode on macOS or Linux:

```sh
mkdir -p ~/.config/opencode/skills/zigbee2mqtt
cp SKILL.md ~/.config/opencode/skills/zigbee2mqtt/
cp -R reference ~/.config/opencode/skills/zigbee2mqtt/
```

For another harness, substitute its skills directory in these commands. Check that the destination does not already contain a different skill before copying. Restart the harness or reload its skills if necessary.

To update, compare the installed copy with the repository, back up any local changes, and copy the current files again. Copies are independent and do not update automatically. Remove obsolete reference files deliberately after reviewing them.

For an AI agent: identify the target harness and destination, check for existing files and local instructions, and obtain approval before overwriting anything. Copy the skill and references, then verify that the harness can discover the skill; report any discovery check that cannot be performed.

## Sources

- [Zigbee2MQTT documentation](https://github.com/Koenkk/zigbee2mqtt.io)
- [Zigbee2MQTT application](https://github.com/Koenkk/zigbee2mqtt)

## License

MIT; see [LICENSE](reference/LICENSE). The license is included when copying `reference/`.
