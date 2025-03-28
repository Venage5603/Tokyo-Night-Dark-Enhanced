# Contributing to Tokyo Night Dark Enhanced

Thank you for your interest in contributing to Tokyo Night Dark Enhanced! This document provides guidelines and instructions for contributing to this VS Code theme.

## Getting Started

1. **Fork the repository** on GitHub
2. **Clone your fork** to your local machine
3. **Install dependencies** with `npm install`
4. **Make your changes** to the theme files

## Development Workflow

### Theme Files

The main theme file is located at `themes/tokyo-night-dark-enhanced-color-theme.json`. This is where all color definitions are stored.

### Testing Your Changes

To test your changes:

1. Press `F5` in VS Code to launch a new Extension Development Host window
2. In the new window, go to `Preferences > Color Theme` and select "Tokyo Night Dark Enhanced"
3. Make changes to the theme file and save - the changes will be reflected immediately in the development window

### Building the Extension

To build the extension locally:

```bash
npm run package
```

This will create a `.vsix` file that you can install in VS Code.

## Pull Request Process

1. **Create a branch** for your changes
2. **Make your changes** and commit them with descriptive commit messages
3. **Push your branch** to your fork
4. **Create a pull request** to the main repository

Please follow these guidelines for commit messages:

- Use the present tense ("Add feature" not "Added feature")
- Use the imperative mood ("Move cursor to..." not "Moves cursor to...")
- Limit the first line to 72 characters or less
- Reference issues and pull requests liberally after the first line

## Release Process

Releases are managed by the maintainers using GitHub Actions:

1. Version bumping is done using the "Version Bump" workflow
2. Releases are created when a tag is pushed with the format `v*`
3. The extension is automatically published to the VS Code Marketplace

## Code of Conduct

Please be respectful and considerate of others when contributing to this project. We aim to foster an inclusive and welcoming community.

## Questions?

If you have any questions or need help, please open an issue on GitHub.
