# Workflows
**Reusable Workflows for Uitsmijter**

This repository contains reusable Workflows for various Uitsmijter projects.

## Workflows
**Issues-Mattermost**
If an Issue is created, a Mattermost notification will be sent to `WEBHOOK`.
```yaml
jobs:
  Notify:
    uses: uitsmijter/workflows/.github/workflows/issues-mattermost.yaml@main
    secrets:
      WEBHOOK: ${{ secrets.MATTERMOST_WEBHOOK }}
```
