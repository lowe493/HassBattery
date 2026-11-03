# Battery status entity changes

This source revision adds a `status_entity` option to the Beautiful Battery card.

- The visual editor exposes a Home Assistant entity selector labelled “Battery status entity”.
- The selected entity takes priority over power-direction and battery-attribute detection.
- Accepted states are `charging`, `discharging`, and `idle` (case-insensitive; surrounding whitespace is ignored).
- Any other or unavailable state falls back to the existing automatic detection logic.

Example:

```yaml
type: custom:beautiful-battery
entity: sensor.battery_level
status_entity: sensor.battery_status
show_status: true
```

## Build

Run from the repository root with Node.js/npm installed:

```sh
npm ci
npm run build
```

The build output is `dist/beautiful-battery.js`.

**Important:** This source-only archive intentionally does not include `dist/beautiful-battery.js`, because the previous archive contained the original, unmodified compiled bundle. Do not install the old bundle expecting the new status entity feature to work.
