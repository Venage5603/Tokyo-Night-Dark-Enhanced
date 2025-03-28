# Dependabot Configuration

This document explains the Dependabot configuration for the Tokyo Night Dark Enhanced repository.

## Overview

Dependabot is configured to automatically check for updates to:

- GitHub Actions workflows
- NPM dependencies

## Configuration Details

### Schedule

Both GitHub Actions and NPM dependencies are checked weekly on Mondays at 9:00 AM UTC. This schedule was chosen to:

- Reduce noise from daily updates
- Ensure updates are processed at the beginning of the work week
- Batch similar updates together

### Pull Request Limits

A maximum of 10 open pull requests are allowed for each ecosystem to prevent overwhelming the repository with updates.

### Commit Messages

Commit messages follow the [Conventional Commits](https://www.conventionalcommits.org/) format:

- GitHub Actions: `ci(deps): update [dependency]`
- NPM dependencies: `build(deps): update [dependency]`

### Reviewers

All Dependabot pull requests are automatically assigned to the repository owner for review.

### Labels

Pull requests are labeled based on the type of dependency:

- All PRs: `dependencies`
- GitHub Actions: `github-actions`
- NPM: `npm`

### Groups

Dependencies are grouped to reduce the number of pull requests:

- GitHub Actions: Minor and patch updates are grouped together
- NPM: Development and production dependencies are grouped separately

### Versioning Strategy

For NPM dependencies:

- The versioning strategy is set to "widen"
- This means that version ranges (e.g., `^1.2.3`) will be maintained rather than pinned to specific versions

### Ignored Updates

Major version updates for NPM dependencies are ignored by default to prevent breaking changes. These should be manually reviewed and updated when needed.

## Managing Dependabot

### Approving Updates

Review each Dependabot pull request carefully before approving:

1. Check the changelog or release notes for the updated dependency
2. Verify that the update doesn't introduce breaking changes
3. Run tests to ensure compatibility

### Customizing Behavior

To modify Dependabot's behavior:

1. Edit the `.github/dependabot.yml` file
2. Commit and push the changes
3. Dependabot will use the updated configuration for future checks

### Disabling Updates

To temporarily disable updates for a specific dependency, add it to the `ignore` section in the configuration file.
