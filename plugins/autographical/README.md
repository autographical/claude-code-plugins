# Autographical

Gives Claude context on your activity (browsing, saves, AI chats, attention) from [Autographical](https://autographical.ai) via MCP.

## Skills

### `/whats-up` — Activity Summary

Fetches your recent activity and summarizes what you've been working on. Use it when starting a session, picking up where you left off, or to see what you've been researching.

Presents:
- **Active threads** grouped by topic/theme
- **Momentum** — which threads have the most recent activity
- **Suggestions** — what to pick up next based on activity patterns

## Installation

Add the Autographical marketplace, then install:

```
/plugin marketplace add autographical/claude-code-plugins
/plugin install autographical@autographical
```

You'll be prompted for your Autographical API key during installation.

## Configuration

### Configuration methods

#### Claude Code native plugin configuration

By default Claude Code manages plugin variables and secrets via its built in `/plugin` mechanism.

#### Environment variables

You can override plugin configuration for each Claude Code instance by setting environment variables.

```sh
AUTOGRAPHICAL_MCP_URL=... claude
```

### Configuration options

#### MCP URL

Defaults to Autographical Cloud US data region (`https://api.autographical.ai/mcp`). Override with:

- `AUTOGRAPHICAL_MCP_URL` environment variable

#### API Key

Set during plugin installation via Claude Code's built-in plugin configuration. Override with:

- `AUTOGRAPHICAL_API_KEY` environment variable
