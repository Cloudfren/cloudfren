# Task tracker: GitHub Projects

All tasks, bugs, and feature requests for this repository are tracked directly as draft items in the `cloudfren` GitHub Project: https://github.com/orgs/Cloudfren/projects/1. The Project is the canonical task tracker; do not create GitHub Issues for routine project work.

Use the GitHub CLI (`gh`) for operations. Run commands from this repository or specify `--owner Cloudfren` explicitly. The configured project number is `1`.

## Conventions

- **List tasks**: `gh project item-list 1 --owner Cloudfren --format json`.
- **Create a task**: `gh project item-create 1 --owner Cloudfren --title "..." --body "..."`.
- **Update a task**: edit the draft item in the GitHub Projects web UI. For linked issues, edit the issue only if the user explicitly asks; task tracking should otherwise remain in draft items.
- **Change status / priority**: use the Project fields in the GitHub Projects web UI or supported `gh project item-edit` commands. Confirm available fields and options before changing them.
- **Remove an item**: only on explicit user request, using the item ID with `gh project item-delete 1 --owner Cloudfren --id <item-id>`.
- **Project access**: Project commands may require `project` token scope. If access is denied, report the missing scope rather than switching trackers.

Do not create a new Project unless the user asks or confirms one is needed. Do not convert draft items into Issues unless the user explicitly requests it.

## When a skill says "publish to the issue tracker"

Create a draft item in the `cloudfren` GitHub Project.

## When a skill says "fetch the relevant ticket"

Find the draft item in the Project with `gh project item-list 1 --owner Cloudfren --format json`.
