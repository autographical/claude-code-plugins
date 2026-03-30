# Autographical Collect

Collects Claude Code session activity and sends it to [Autographical](https://autographical.ai).

## What it collects

Hooks into Claude Code session events to capture:
- **Prompt submissions** — when you send a prompt
- **Turn completions** — when Claude returns a response
- **Session ends** — session transcript and metadata

## Installation

Add the Autographical marketplace, then install:

```
/plugin marketplace add autographical/claude-code-plugins
/plugin install autographical-collect@autographical
```

You'll be prompted for your Autographical ingest token during installation.

## Configuration

### Configuration methods

#### Claude Code native plugin configuration

By default Claude Code manages plugin variables and secrets via its built in `/plugin` mechanism.

#### Shared config file

The plugin automatically reads configuration from a user directory level configuration file if it exists: `~/.config/autographical/config.json`:

```json
{
  "ingestUrl": "https://ingest.autographical.ai",
  "ingestToken": "your-token"
}
```

#### Environment variables

You can override plugin configuration for each Claude Code instance by setting environment variables.

```sh
AUTOGRAPHICAL_INGEST_URL=... claude
```

### Configuration options

### Ingest URL

Defaults to Autographical Cloud US data region (`https://ingest.autographical.ai`). Override with:

- `AUTOGRAPHICAL_INGEST_URL` environment variable
- `ingestUrl` in `~/.config/autographical/config.json`

### Ingest Token

Set during plugin installation via Claude Code's built-in plugin configuration. Override with:

- `AUTOGRAPHICAL_INGEST_TOKEN` environment variable
- `ingestToken` in `~/.config/autographical/config.json`

If no ingest token is configured, the plugin silently no-ops.
