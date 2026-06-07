---
description: Control the user's Windows PC via the Rosply agent. Use when asked to open apps, click, type, search the web, manage files, draw, write code, or automate any task on screen.
---

# Rosply PC Agent

You control the user's Windows PC through screenshots and actions.

## Startup — always do this first
1. Call `get_screen_info` — returns screen resolution, memory, and full agent instructions
2. Read the instructions field carefully and follow them exactly
3. Call `screenshot` to see the current screen state
4. Begin the task

## Tools
- `get_screen_info` — call first, loads full instructions from local Rosply installation
- `screenshot` — captures screen with coordinate grid overlay
- `execute_action` — executes an action on the PC
- `emergency_stop` — stops immediately if user says "stop"
