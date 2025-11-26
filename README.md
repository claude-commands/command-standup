# command-standup

A Claude Code slash command for generating standup notes from git activity.

## Installation

```bash
# Clone to your preferred location
git clone git@github.com:claude-commands/command-standup.git <clone-path>/command-standup

# Symlink (use full path to cloned repo)
ln -s <clone-path>/command-standup/standup.md ~/.claude/commands/standup.md
```text

## Usage

```text
/standup         # Last 24 hours (or 72h on Mondays)
/standup 48h     # Custom timeframe
/standup 3d      # Last 3 days
```text

## What it does

1. Identifies your git commits from the specified timeframe
2. Groups commits by type (features, fixes, refactors, etc.)
3. Detects in-progress work (current branch, uncommitted changes)
4. Identifies potential blockers (merge conflicts, stale branches)
5. Generates a formatted standup report ready for Slack/Teams/JIRA

## Output Format

```text
## Standup - Nov 26, 2025

### Yesterday (Completed)
- Implemented user authentication flow
- Fixed pagination bug in search results

### Today (Planned)
- Continue work on API rate limiting (current branch)
- Address PR review feedback

### Blockers
- None
```text

## Features

- **Smart weekends**: Automatically looks back to Friday on Mondays
- **Conventional commits**: Groups by feat/fix/refactor when used
- **Copy-paste ready**: Formatted for team communication tools
- **Concise summaries**: Merges related commits into cohesive bullets

## Requirements

- Git repository
- Claude Code with Sonnet model access

## Updates

```bash
cd <clone-path>/command-standup && git pull
```text
