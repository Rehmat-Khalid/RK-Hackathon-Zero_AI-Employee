# Company Handbook

## Purpose

This file defines how the AI Employee behaves when processing files and tasks. It serves as the single source of truth for all operational rules and ensures consistent, predictable behavior across all automated actions.

---

## File Processing Rules

- When a new file appears in `/Needs_Action`, read it and determine what action is needed
- Create a summary and move the processed result to `/Done`
- Update `Dashboard.md` after every action

---

## Priority Keywords

| Priority | Keywords |
|----------|----------|
| 🔴 Critical | urgent, emergency, asap |
| 🟠 High | important, deadline, invoice |
| 🟡 Medium | question, update, follow-up |
| 🟢 Low | fyi, no rush |

---

## Naming Convention

- **Needs_Action:** `TYPE_description_YYYYMMDD_HHMMSS.md`
- **Done:** `DONE_TYPE_description_YYYYMMDD_HHMMSS.md`
