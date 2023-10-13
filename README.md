# Workflows
**Reusable Workflows for Uitsmijter**

This repository contains reusable workflows for various Uitsmijter projects.

## Workflows
**Issues-Mattermost**
If an Issue is created, a Mattermost notification will be sent to `WEBHOOK`.
```yaml
name: Issues
on:
  issues:
    types:
      - opened
      - edited
      - closed
      - reopened
  issue_comment:
    types:
      - created
      - edited

jobs:
  Mattermost:
    uses: uitsmijter/workflows/.github/workflows/issues-mattermost.yaml@main
    secrets:
      WEBHOOK: ${{ secrets.MATTERMOST_WEBHOOK }}
```
