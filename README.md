# gh-react

✨ Add emoji reactions to PR comments from your terminal using GitHub CLI.

A GitHub CLI extension that allows you to quickly react to pull request comments, reviews, and descriptions without leaving your terminal.

## Features

- 🎯 React to **all types of PR content**:
  - PR descriptions/body
  - General PR comments
  - Inline code review comments
  - Review summary comments
- 🚀 Dynamic PR number support
- 🔍 Automatic comment type detection
- ✅ Comprehensive error handling
- 📋 Lists all available comments with IDs

## Install

```bash
gh extension install manishraj27/gh-react
```

## Usage

### Basic Usage

```bash
gh react <pr_number>
```

**Example:**
```bash
gh react 23
```

### What happens:

1. **Fetches all comments** from the specified PR
2. **Lists comments** with their IDs and authors
3. **Prompts for comment ID** to react to
4. **Asks for reaction type** from available options
5. **Sends the reaction** via GitHub API

### Example Output

```bash
$ gh react 23
Fetching comments for PR #23...
Checking if PR #23 exists...
Fetching comments...
PR_BODY|23|manishraj27: fix: update homepage URL in package.json
ISSUE|3045853431|manishraj27: test

Enter comment ID to react to: 3045853431
Pick a reaction: (+1, -1, laugh, heart, hooray, rocket, eyes)
Reaction: +1
Sending reaction...
Done! 👍
```

## Available Reactions

| Reaction | Description |
|----------|-------------|
| `+1` | 👍 Thumbs up |
| `-1` | 👎 Thumbs down |
| `laugh` | 😄 Laugh |
| `heart` | ❤️ Heart |
| `hooray` | 🎉 Hooray |
| `rocket` | 🚀 Rocket |
| `eyes` | 👀 Eyes |

## Comment Types Supported

- **PR_BODY**: The main PR description/body
- **ISSUE**: General comments on the PR conversation
- **REVIEW**: Inline comments on specific lines of code
- **REVIEW_SUMMARY**: Comments submitted with code reviews

## Requirements

- [GitHub CLI](https://cli.github.com/) installed and authenticated
- Access to the repository containing the PR
- Bash shell environment

## Error Handling

The extension handles various scenarios:
- Invalid or non-existent PR numbers
- PRs with no comments
- Authentication issues
- Network connectivity problems

## Contributing

1. Fork the repository
2. Create your feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

MIT License - see LICENSE file for details.
