# samkari-plugins

Mohammad Samkari's Claude plugins marketplace.

```
/plugin marketplace add msamkari/samkari-plugins
```

| Plugin | Install | Repo |
|---|---|---|
| `persistent-memory` | `/plugin install persistent-memory@samkari-plugins` | [persistent-memory-plugin](https://github.com/msamkari/persistent-memory-plugin) |
| `structured-handover` | `/plugin install structured-handover@samkari-plugins` | [structured-handover-doc-skill](https://github.com/msamkari/structured-handover-doc-skill) |

## Adding a plugin

Add an entry to the `plugins` array in `.claude-plugin/marketplace.json` that points at the plugin's own repository (`"source": {"source": "github", "repo": "owner/repo"}`). Each plugin keeps its own repo; this repo is only the index.

Update with `/plugin marketplace update samkari-plugins`.

## Versioning

Every plugin follows [semantic versioning](https://semver.org) (`MAJOR.MINOR.PATCH`) and keeps its version in its own `.claude-plugin/plugin.json`.

- `PATCH` (1.0.0 → 1.0.1): bug fixes and wording.
- `MINOR` (1.0.0 → 1.1.0): new features that keep working as before.
- `MAJOR` (1.0.0 → 2.0.0): changes that break existing use.

Claude Code only offers an update when the version number goes up, so bump it on every release. Each release is also tagged in the plugin's repo (`v1.0.0`, `v1.0.1`, ...).

| Plugin | Current version |
|---|---|
| `persistent-memory` | 1.0.0 |
| `structured-handover` | 1.0.0 |
