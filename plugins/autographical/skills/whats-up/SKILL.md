---
description: Fetch recent user activity (browsing, saves, AI chats, attention) from Autographical and summarize what the user has been working on. Use when starting a session, when the user wants to know what they've been researching, or to pick up where they left off.
---

# What's Up — Activity Summary

You have access to the user's activity history via the Autographical MCP server (browsing visits, page views, saves, AI chat conversations, focus/attention time). Use the MCP tools to fetch recent activity, then synthesize it into actionable context.

## Steps

1. Call the `recent_activity` MCP tool to fetch recent sessions and top resources.

2. If the user provided arguments via `$ARGUMENTS`, also call the `search` MCP tool with those arguments.

3. Analyze the output and present:
   - **Active threads**: Group sessions by topic/theme. Identify what the user has been researching or working on.
   - **Momentum**: Which threads have the most recent activity or attention? What seems to be in-progress?
   - **Suggestions**: Based on the activity pattern, suggest what to pick up next. Look for:
     - Research that seems incomplete (few resources, short focus times)
     - Topics with heavy recent attention (likely actively working on)
     - Threads that were active but then dropped off (might want to revisit)

4. Keep your summary concise — a few sentences per thread, not an exhaustive list of every URL.
