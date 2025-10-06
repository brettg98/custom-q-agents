# Context Conventions

## Project Summary
This repository contains custom Q agents for Amazon Q CLI, focusing on improving agent maintainability through external prompt files and streamlined resource management.

## Required Content Structure

### Technical Details Section
- Specific file paths modified
- Commands executed
- Implementation approaches used

### Current State Section  
- What was completed
- What remains to be done
- References to outstanding requests

### Decision Rationale Section
- Why specific choices were made
- Before/after comparisons
- Impact of changes

## Purpose
Event-based context logging for project work sessions, decisions, and troubleshooting.

## File Format
- **Format**: `YYYY-MM-DD-context-name.md`
- **Location**: `.orbit/context/` directory in project root
- **Purpose**: Specific events, work sessions, decisions, or troubleshooting

## Directory Structure
```
.orbit/
├── context/
│   ├── 2025-09-30-added-new-permissions.md
│   ├── 2025-03-14-troubleshooting-access-issue.md
│   └── 2025-05-17-added-new-cfn-template.md
├── git/
└── shared/
```

## Naming Examples
- `2025-09-30-added-new-permissions.md`
- `2025-03-14-troubleshooting-access-issue.md`
- `2025-05-17-added-new-cfn-template.md`
- `2025-09-30-work-session-auth-module.md`

## Content Structure
- Always include date/timestamp
- Use clear section headers
- Link related files/PRs when relevant
- Tag with keywords for searchability
