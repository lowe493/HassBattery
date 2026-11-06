# Horizontal compact layout build notes

This revision adds an optional `layout` configuration setting:

- `vertical` (default): existing vertical battery design.
- `horizontal_compact`: horizontal battery graphic on the left, percentage to its right, and status centred underneath.

The visual editor exposes the setting under Appearance. Existing `status_entity` support is retained.

To build from the repository root:

```sh
npm ci
npm run build
```

The compiled Home Assistant resource is `dist/beautiful-battery.js`.

The build could not be run in the preparation environment because npm dependency installation timed out. The `dist/beautiful-battery.js` included in the original uploaded archive is therefore not updated and must not be deployed as the new build. Build locally before installing.
