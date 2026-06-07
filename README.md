# Rosply Agent — Claude Code Plugin

Control your Windows PC from Claude Code. Rosply provides the eyes (screen capture) and hands (mouse, keyboard, apps). Claude Code provides the brain.

## Requirements

- [Rosply](https://rosply.com) installed and running on your PC
- Claude Code

## Install

```
/plugin marketplace add harkixsha/rosply-agent-plugin
/plugin install rosply-agent@harkixsha-plugins
```

## Usage

Once installed, Claude Code can see your screen and control your PC. Just describe what you want done:

```
Open Chrome and search for the latest AI news
```
```
Open Notepad and write a summary of my last meeting
```
```
Go to my Downloads folder and tell me what files are there
```

## Model

Default: `claude-haiku-4-5`. Claude Code is the brain, no OpenRouter key needed for agent reasoning when using this plugin.

## Emergency stop

Press `Ctrl+H` at any time to immediately stop the agent.

---

Made by [Harkixsha](https://harkixsha.com)
