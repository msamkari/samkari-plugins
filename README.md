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
