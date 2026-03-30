# Autographical Plugins for Claude Code

Plugins that connect [Claude Code](https://claude.ai/code) to [Autographical](https://autographical.ai) for context sharing and session collection.

## Plugins

| Plugin | Description |
|--------|-------------|
| [autographical](./plugins/autographical/) | Give Claude context on your activity (browsing, saves, AI chats, attention) from Autographical via MCP |
| [autographical-collect](./plugins/autographical-collect/) | Collect Claude Code session activity to Autographical |

## Installation

Add this marketplace:

```
/plugin marketplace add autographical/claude-code-plugins
```

Then install plugins:

```
/plugin install autographical@autographical
/plugin install autographical-collect@autographical
```

See each plugin's README for configuration details.
