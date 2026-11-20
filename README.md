# samkari-plugins

Mohammad Samkari's Claude plugins marketplace.

```
/plugin marketplace add msamkari/samkari-plugins
```

| Plugin | Install | Repo |
|---|---|---|
| `persistent-memory` | `/plugin install persistent-memory@samkari-plugins` | [persistent-memory-plugin](https://github.com/msamkari/persistent-memory-plugin) |
| `baton` | `/plugin install baton@samkari-plugins` | [baton](https://github.com/msamkari/baton) |
| `vitals` | `/plugin install vitals@samkari-plugins` | [vitals](https://github.com/msamkari/vitals) |
| `clipscope` | `/plugin install clipscope@samkari-plugins` | [clipscope](https://github.com/msamkari/clipscope) |
| `nightshift` | `/plugin install nightshift@samkari-plugins` | [nightshift](https://github.com/msamkari/nightshift) |
| `ctxguard` | `/plugin install ctxguard@samkari-plugins` | [ctxguard](https://github.com/msamkari/ctxguard) |
| `lahja` | `/plugin install lahja@samkari-plugins` | [lahja](https://github.com/msamkari/lahja) |
| `lahja-voice` | `/plugin install lahja-voice@samkari-plugins` | [lahja-voice](https://github.com/msamkari/lahja-voice) |
| `loom` | `/plugin install loom@samkari-plugins` | [loom](https://github.com/msamkari/loom) |
| `relay` | `/plugin install relay@samkari-plugins` | [relay](https://github.com/msamkari/relay) |
| `keyframe-kit` | `/plugin install keyframe-kit@samkari-plugins` | [keyframe-kit](https://github.com/msamkari/keyframe-kit) |

## Adding a plugin

Add an entry to the `plugins` array in `.claude-plugin/marketplace.json` that points at the plugin's own repository (`"source": {"source": "url", "url": "https://github.com/owner/repo.git"}`; HTTPS avoids SSH host-key errors on machines without SSH set up). Each plugin keeps its own repo; this repo is only the index.

Update with `/plugin marketplace update samkari-plugins`.

## Versioning

Every plugin follows [semantic versioning](https://semver.org) (`MAJOR.MINOR.PATCH`) and keeps its version in its own `.claude-plugin/plugin.json`.

- `PATCH` (1.0.0 → 1.0.1): bug fixes and wording.
- `MINOR` (1.0.0 → 1.1.0): new features that keep working as before.
- `MAJOR` (1.0.0 → 2.0.0): changes that break existing use.

Claude Code only offers an update when the version number goes up, so bump it on every release. For each release, also create a GitHub Release in the plugin's repo (it creates the tag: `v1.0.0`, `v1.0.1`, ...). This step is manual: automated sessions cannot create tags or releases.

The current version of each plugin is in its own repository (latest GitHub Release) and in `/plugin list`; this README no longer lists versions.
