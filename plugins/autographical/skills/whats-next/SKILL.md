---
description: Suggest what to work on next based on recent activity and current context. Use when the user is between tasks, at a decision point, wants direction on where to focus, or asks what to do next.
---

# What's Next

The user is at a crossroads — they've finished something, they're stuck, or they're starting fresh and want direction. Fetch their recent activity, consider the current context, and lead with a recommendation.

## Context

Working directory: !`pwd`
Git repo: !`basename $(git rev-parse --show-toplevel 2>/dev/null) 2>/dev/null || echo "not a git repo"`
Git branch: !`git branch --show-current 2>/dev/null || echo "n/a"`
Recent commits: !`git log --oneline -5 2>/dev/null || echo "n/a"`

## Data

1. Call the `recent_activity` MCP tool to fetch recent sessions and top resources.

2. If the user provided arguments via `$ARGUMENTS`, also call the `search` MCP tool with those arguments.

3. If a specific path or resource looks relevant, use `get_resource` or `get_session` to drill deeper.

## Synthesis

Lead with what you'd suggest the user do next, and why. You have full latitude — don't follow a rigid template. Some angles:

- Which paths have open loops — research that seems incomplete, questions unanswered?
- Which paths have been active but dropped off — worth revisiting or consciously shelving?
- What's the relationship between recent activity and the current working context (repo, branch)?
- Are there paths that connect to each other in ways the user might not have noticed?

Be opinionated. The user wants direction, not a data dump. If you see a clear next step, say so. If the current repo/branch connects to an active path, call that out specifically.
