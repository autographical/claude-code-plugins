# Autographical

Gives Claude context on your activity (browsing, saves, AI chats, attention) from [Autographical](https://autographical.ai) via MCP.

## Components

### Skills

#### `/whats-up` — What's been happening

Fetches your recent activity and brings context into the session. Use it when starting a session, picking up where you left off, or mid-session to refresh with the latest activity.

#### `/whats-next` — What to do next

Suggests what to work on next based on your recent activity and current working context (repo, branch, recent commits). Use it at a decision point, between tasks, or when you want direction.

### MCP

Installs tools to connect to Autographical API and traverse the activity stream and knowledge graph.


## Installation

Add the Autographical marketplace, then install:

```
/plugin marketplace add autographical/claude-code-plugins
/plugin install autographical@autographical
```

## Authentication

### Interactive (default)

Authentication is handled automatically via OAuth. After installing the plugin, open the MCP panel and authenticate:

```
/mcp
```

Claude Code will open your browser to sign in to Autographical. Tokens are managed by Claude Code directly (stored securely in your system keychain and refreshed automatically).

### Headless (remote agents, CI, scheduled tasks)

For non-interactive environments where OAuth isn't available, configure the MCP server directly with an API key:

```bash
claude mcp add --transport http autographical https://api.autographical.ai/mcp \
  --header "Authorization: Bearer <your-api-key>"
```

Create an API key in your Autographical user settings.

## Configuration

### MCP URL

Defaults to Autographical Cloud US data region (`https://api.autographical.ai/mcp`). Override with:

- `AUTOGRAPHICAL_MCP_URL` environment variable
