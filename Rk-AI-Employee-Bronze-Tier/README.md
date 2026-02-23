# Personal AI Employee — Bronze Tier

## What It Is

A personal AI employee that monitors a file drop folder and processes items using Claude Code and Obsidian. When you drop files into a watched folder, the system automatically creates action items, classifies them by priority, processes them, and maintains a real-time dashboard of activity.

## Architecture

```
┌─────────────┐    ┌──────────────┐    ┌───────────────┐    ┌─────────────┐    ┌────────┐
│ Drop Folder │ -> │ File Watcher │ -> │ /Needs_Action │ -> │ Claude Code │ -> │ /Done  │
│ ~/AI_Drop   │    │  (watchdog)  │    │               │    │  (skills)   │    │        │
└─────────────┘    └──────────────┘    └───────────────┘    └─────────────┘    └────────┘
```

## Tech Stack

| Component | Purpose |
|-----------|---------|
| Claude Code | AI processing and task execution |
| Obsidian | Vault interface and dashboard viewing |
| Python + watchdog | File system monitoring |

## Prerequisites

- Claude Code
- Python 3.13+
- Obsidian
- Node.js v24+

## Quick Start

```bash
# 1. Clone repo
git clone <repo-url>
cd AI_Employee_Vault

# 2. Install dependencies
uv sync

# 3. Open vault in Obsidian
# File -> Open Vault -> Select this folder

# 4. Configure environment
cp .env.example .env

# 5. Start the file watcher
python watchers/filesystem_watcher.py

# 6. Test it
# Drop any file into ~/AI_Drop and watch it appear in /Needs_Action
```

## Tier

**Bronze** — File monitoring and basic processing.

## Folder Structure

```
AI_Employee_Vault/
├── Inbox/              # Raw incoming items
├── Needs_Action/       # Items ready for processing
├── Done/               # Completed items
├── watchers/           # Python file watchers
├── .claude/skills/     # Agent skills
├── Dashboard.md        # Real-time status
├── Company_Handbook.md # Rules of engagement
└── CLAUDE.md           # Claude Code instructions
```

## Agent Skills

| Skill | Description |
|-------|-------------|
| `file-processing` | Process items from /Needs_Action, classify priority, move to /Done |
| `vault-management` | Update Dashboard.md, track file counts, maintain structure |
