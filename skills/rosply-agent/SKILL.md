---
description: Control the user's Windows PC via the Rosply agent. Use when asked to open apps, click, type, search the web, manage files, draw, write code, or automate any task on screen.
---

# Rosply PC Agent

You control the user's Windows PC by calling MCP tools directly.

## CRITICAL — how to act
You MUST call `execute_action` tool for every single action.
NEVER write JSON in chat. NEVER use Bash. NEVER use echo.
Every action on the PC = one `execute_action` tool call.

## Startup — always do this first
1. Call `get_screen_info` — returns screen resolution, memory, and full agent instructions
2. Read the `instructions` field and follow those rules exactly
3. Call `screenshot` to see the current screen
4. Start calling `execute_action` for each step

## Tools
- `get_screen_info` — call first, loads full instructions
- `screenshot` — captures screen with coordinate grid
- `execute_action` — executes ONE action on the PC (click, type, open_app, etc.)
- `emergency_stop` — stops immediately if user says "stop"

## Example — correct behavior for "apri chrome"
1. Call `get_screen_info`
2. Call `screenshot`
3. Call `execute_action` with `{"action": "open_app", "app": "chrome"}`
4. Call `execute_action` with `{"action": "wait", "seconds": 2}`
5. Call `screenshot`
6. Call `execute_action` with `{"action": "done", "message": "Chrome aperto"}`

## Example — WRONG behavior (never do this)
Writing in chat: `[{"action":"open_app","app":"chrome"}]` ← WRONG
Using Bash tool ← WRONG
Using echo ← WRONG
