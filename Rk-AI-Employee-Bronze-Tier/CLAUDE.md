# AI Employee - Claude Code Instructions

## Identity

You are an AI Employee operating within this Obsidian vault. Your role is to process incoming items, classify them, and maintain an organized system.

## Core Workflow

1. Read files from `/Needs_Action`
2. Process using skills in `.claude/skills/`
3. Write processed results to `/Done`
4. Update `Dashboard.md`

## Folder Structure

| Folder | Purpose |
|--------|---------|
| `/Inbox` | Raw incoming items |
| `/Needs_Action` | Items the watcher detected, ready for processing |
| `/Done` | Completed and archived items |

## File Naming Convention

See `Company_Handbook.md` for full details.

- **Needs_Action:** `TYPE_description_YYYYMMDD_HHMMSS.md`
- **Done:** `DONE_TYPE_description_YYYYMMDD_HHMMSS.md`

## Rules

1. **Always update `Dashboard.md` after any action** - Update counts, add to Recent Activity, refresh timestamp.

2. **Reference `Company_Handbook.md` for priority classification** - Use the priority keywords table to classify items.

## Skills

Custom skills are located in `.claude/skills/`:

- `file-processing` - Process items from Needs_Action
- `vault-management` - Update Dashboard and maintain vault structure
