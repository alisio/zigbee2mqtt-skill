# Zigbee2MQTT skill

An agent skill for operating and integrating Zigbee2MQTT. It covers configuration, MQTT, pairing, adapters, updates, and troubleshooting. The reference targets Zigbee2MQTT 2.x; consult the linked upstream documentation for the installed version.

## Installation

Clone the repository and enter its directory:

```sh
git clone https://github.com/alisio/zigbee2mqtt-skill.git
cd zigbee2mqtt-skill
```

Copy `SKILL.md` and `reference/` into a directory named `zigbee2mqtt` under your harness's skills directory. The skill and its references must remain together. The following are common user-level locations; consult your harness documentation for the location supported by your version:

| Harness | Skill directory |
| --- | --- |
| OpenCode | `~/.config/opencode/skills/zigbee2mqtt` |
| Claude Code | `~/.claude/skills/zigbee2mqtt` |
| Codex | `~/.agents/skills/zigbee2mqtt` |

Before copying, check whether the destination already exists. Copying over an existing skill can overwrite its files; back up any changes you want to keep.

For example, from the root of this repository, to install for OpenCode on macOS or Linux:

```sh
mkdir -p ~/.config/opencode/skills/zigbee2mqtt
cp SKILL.md ~/.config/opencode/skills/zigbee2mqtt/
cp -R reference ~/.config/opencode/skills/zigbee2mqtt/
```

For another harness, substitute its skills directory in these commands. Restart the harness or reload its skills if necessary.

## First use

Ask your agent, for example: "Use the zigbee2mqtt skill to explain how to pair a new device safely." Check that the harness loads the skill and that the response refers to the relevant pairing guidance. Invocation and discovery indicators depend on the harness; consult its documentation if the skill is not found.

## Updating

Copies are independent and do not update automatically. From the repository root, compare the installed OpenCode copy with the current repository files:

```sh
diff -u ~/.config/opencode/skills/zigbee2mqtt/SKILL.md SKILL.md
diff -r ~/.config/opencode/skills/zigbee2mqtt/reference reference
```

For another harness, substitute its skill directory. Differences include both local edits and upstream changes; back up anything you want to keep before copying the files again. Review and remove obsolete installed reference files deliberately; copying does not remove them.

For an AI agent: identify the target harness and destination, check for existing files and local instructions, and obtain approval before overwriting anything. Copy the skill and references, then verify that the harness can discover the skill; report any discovery check that cannot be performed.

## Sources

- [Zigbee2MQTT documentation](https://github.com/Koenkk/zigbee2mqtt.io)
- [Zigbee2MQTT application](https://github.com/Koenkk/zigbee2mqtt)

## License

MIT; see [LICENSE](reference/LICENSE). The license is included when copying `reference/`.
