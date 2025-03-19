# GitHub Workflows for Tokyo Night Dark Enhanced

This directory contains GitHub Actions workflows that automate various tasks for the Tokyo Night Dark Enhanced VS Code theme.

## Workflows

### Build Extension (`build.yml`)
- **Triggers**: Push to main, pull requests to main, manual trigger
- **Purpose**: Builds the extension and uploads the VSIX file as an artifact
- **Key steps**:
  - Checkout code
  - Setup Node.js
  - Install dependencies
  - Build the extension
  - Upload the VSIX file as an artifact

### Lint (`lint.yml`)
- **Triggers**: Push to main, pull requests to main, manual trigger
- **Purpose**: Validates JSON files to ensure they are properly formatted
- **Key steps**:
  - Checkout code
  - Setup Node.js
  - Install dependencies
  - Validate theme JSON files
  - Validate package.json

### Release Extension (`release.yml`)
- **Triggers**: When a tag with format `v*` is pushed
- **Purpose**: Publishes the extension to the VS Code Marketplace and creates a GitHub release
- **Key steps**:
  - Checkout code
  - Setup Node.js
  - Install dependencies
  - Verify tag version matches package.json version
  - Package the extension
  - Publish to VS Code Marketplace
  - Create GitHub release with the VSIX file attached

### Version Bump (`version-bump.yml`)
- **Triggers**: Manual trigger with version bump type selection
- **Purpose**: Automates version bumping and changelog generation
- **Key steps**:
  - Checkout code
  - Setup Node.js
  - Install dependencies
  - Bump version using standard-version
  - Push changes
  - Create a pull request for the release

## Dependabot Configuration

The `dependabot.yml` file configures Dependabot to:
- Update GitHub Actions dependencies daily
- Update npm dependencies daily
- Limit open pull requests to 10 for each ecosystem
- Use specific commit message prefixes
- Assign reviewers to pull requests

## Required Secrets

- `VSCE_PAT`: Personal Access Token for publishing to the VS Code Marketplace
