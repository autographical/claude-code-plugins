---
description: Fetch recent activity from Autographical and bring the user's context into the session. Use at the start of a session to catch up, or mid-session to refresh with the latest activity.
---

# What's Up

Fetch recent activity from Autographical and present what's been happening. The activity stream includes everything the user has been doing — browsing, reading, saving, researching — as well as activity from AI sessions the user has been collaborating with. It's the full picture of human + AI work.

## Data

1. Call the `recent_activity` MCP tool to fetch recent sessions and top resources.

2. If the user provided arguments via `$ARGUMENTS`, also call the `search` MCP tool with those arguments to narrow focus.

3. If a session or resource looks particularly relevant, use `get_session` or `get_resource` to get more detail.

## Synthesis

Lead with what you find interesting or notable. You have full latitude in how you read and present the data — don't follow a rigid template. Some things to surface:

- Active threads and topics — what has the user been engaged with, and what have their AI collaborators been working on?
- Momentum — where is attention concentrated? What's in-progress?
- Recency and intensity — what's hot right now vs background threads?

Keep it concise. A few sentences per thread, not an exhaustive list of URLs. The goal is to transfer context to you so the session can build from shared awareness.
