# LIFX Sync Integration

Home Assistant custom integration for the [LIFX Sync add-on](https://github.com/Quinnod345/lifx-sync-ha-addon).

Creates one light entity per group (Bar, Deck, Downlight, etc.) plus an All Lights entity. Each entity calls the add-on's REST API which runs a hardened burst-and-verify sync so all bulbs in a group turn on or off simultaneously.

## Requirements

The [LIFX Sync add-on](https://github.com/Quinnod345/lifx-sync-ha-addon) must be installed and running first.

## Install via HACS

1. HACS → Integrations → ⋮ → Custom repositories
2. Paste `https://github.com/Quinnod345/lifx-sync-integration` — category: **Integration**
3. Download, restart Home Assistant
4. Settings → Devices & Services → Add Integration → **LIFX Sync**
5. Enter `localhost` and `5050`

## Re-discover lights

Settings → Devices & Services → LIFX Sync → **Configure** → tick **Re-discover lights** → Save.

This scans the network, pulls the current names from your bulbs, and reloads all entities with updated groups.
