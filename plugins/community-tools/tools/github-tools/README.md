# GitHub Tools MCP Server

## Overview
MCP server providing integration with GitHub for managing repositories, issues, pull requests, and other GitHub operations directly from Claude.

## Installation
```bash
npm install @mcp/github-tools
# or
pip install mcp-github-tools
```

## Configuration
Set your GitHub token:
```bash
export GITHUB_TOKEN=your_github_token
```

## Tools provided
- `create_issue` — Create issues in GitHub repositories
- `create_pull_request` — Create PRs and manage them
- `list_issues` — List and search issues
- `list_pull_requests` — List and search pull requests
- `get_repository` — Get repository information
- `update_issue` — Update issue details, labels, assignees
- `update_pull_request` — Update PR details
- `add_comment` — Add comments to issues/PRs
- `merge_pull_request` — Merge a pull request
- `create_branch` — Create new branches
- `list_releases` — List repository releases

## Usage Example
Claude can use this to:
- Create issues for bugs found during code review
- Manage pull request workflow
- Update issue status and labels
- Create releases and manage project milestones

## Requirements
- GitHub account with repository access
- GitHub personal access token
- Network access to github.com

## Authentication
Generate a personal access token at: https://github.com/settings/tokens
- Scopes needed: `repo`, `issue`, `pull_request`

## Features
- Full GitHub API access via MCP
- Support for organization and personal repositories
- Labels, milestones, and project management
- Workflow automation
- Release management

## Limitations
- Requires valid GitHub token
- Rate limited by GitHub API (60 requests/hour for unauthenticated)
- Cannot access private repositories without proper permissions
- Some GitHub Enterprise features not supported

## Example
```
User: Create an issue for the bug we found in the authentication module
Claude: [Uses create_issue tool] Created issue #123: "Fix authentication module bug"
```

## Contributing
Submit improvements to the [GitHub Tools repository](https://github.com/community/mcp-github-tools)

## License
MIT
