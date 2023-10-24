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

## Secrets needed
- MATTERMOST_WEBHOOK_URL
- MASTODON_URL
- MASTODON_ACCESS_TOKEN

Set named secrets to your organisation.

## Workflows included
- Build Status to Mastodon: uitsmijter/workflows/.github/workflows/build-mastodon.yaml@main
- Build Status to Mattermost: uitsmijter/workflows/.github/workflows/build-mattermost.yaml@main
- Issue Opened to Mattermost: uitsmijter/workflows/.github/workflows/issues-mattermost.yaml@main
- Pull Request Opend to Mattermost: uitsmijter/workflows/.github/workflows/pullrequest-mattermost.yaml@main
- Release Announcements to Mastodon: uitsmijter/workflows/.github/workflows/release-mastodon.yaml@main

## Used by
[Uitsmijter](https://uitsmijter.io)
[Documentation](https://docs.uitsmijter.io)
[GitHub](https://github.com/uitsmijter/)

## Created by
[aus der Technik](https://ausdertechnik.de)
