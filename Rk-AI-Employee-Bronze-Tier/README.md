🥉 Personal AI Employee — Bronze Tier
📌 Overview

Personal AI Employee is an automated AI-powered assistant that monitors a designated file drop folder and processes incoming items intelligently using Claude Code and Obsidian.

When files are added to the watched directory, the system automatically:

Detects new items

Moves them to a processing queue

Classifies them by priority

Executes AI-driven actions

Updates a real-time dashboard

This creates a lightweight autonomous workflow system.
┌─────────────┐    ┌──────────────┐    ┌───────────────┐    ┌─────────────┐    ┌────────┐
│ Drop Folder │ -> │ File Watcher │ -> │ /Needs_Action │ -> │ Claude Code │ -> │ /Done  │
│ ~/AI_Drop   │    │  (watchdog)  │    │               │    │  (skills)   │    │        │
└─────────────┘    └──────────────┘    └───────────────┘    └─────────────┘    └────────┘
🛠 Tech Stack
Component	Role
Claude Code	AI task processing and automation
Obsidian	Vault interface and dashboard visualization
Python + watchdog	Real-time file system monitoring
Node.js	Runtime support
📦 Prerequisites

Before running the system, ensure you have:

Claude Code installed

Python 3.13+

Obsidian

Node.js v24+
🚀 Quick Start
# 1. Clone repository
git clone <repo-url>
cd AI_Employee_Vault

# 2. Install dependencies
uv sync

# 3. Open vault in Obsidian
# File -> Open Vault -> Select this folder

# 4. Configure environment variables
cp .env.example .env

# 5. Start file watcher
python watchers/filesystem_watcher.py

# 6. Test system
# Drop any file into ~/AI_Drop
# It will automatically move to /Needs_Action and process
🥉 Tier Description

Bronze Tier provides:

Automated file monitoring

Basic AI-powered processing

Priority classification

Dashboard updates

Structured vault organization

📁 Project Structure
AI_Employee_Vault/
├── Inbox/               # Incoming raw items
├── Needs_Action/        # Items queued for AI processing
├── Done/                # Completed and processed items
├── watchers/            # File monitoring scripts
├── .claude/skills/      # AI agent skill definitions
├── Dashboard.md         # Live activity dashboard
├── Company_Handbook.md  # Operational guidelines
└── CLAUDE.md            # Claude Code instructions

🤖 Agent Skills
Skill	Function
file-processing	Processes items, assigns priority, moves to /Done
vault-management	Updates dashboard, tracks file status, maintains structure
