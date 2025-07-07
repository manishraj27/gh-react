# gh-react

✨ Add emoji reactions to PR comments from your terminal using GitHub CLI.

A GitHub CLI extension that allows you to quickly react to pull request comments, reviews, and descriptions without leaving your terminal.

## Features

- 🎯 React to **all types of PR content**:
  - PR descriptions/body
  - General PR comments
  - Inline code review comments
  - Review summary comments
- 🚀 **User-friendly numbered selection** - No more copying long IDs!
- 🌈 **Beautiful colored output** with emojis and visual indicators
- 🔍 Automatic comment type detection
- ✅ Comprehensive error handling and validation
- � Smart progress indicators
- 💡 Helpful tips and guidance

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

1. **🔍 Validates PR** - Checks if the PR exists and you have access
2. **📊 Fetches all content** - Gets PR description, comments, and reviews
3. **📋 Shows numbered list** - Displays all content with easy-to-use numbers
4. **🔢 Simple selection** - Just type a number (1, 2, 3...) instead of long IDs
5. **😊 Pick reaction** - Choose from visual emoji options
6. **🚀 Instant feedback** - Confirms success with direct PR link

### Example Output

```bash
$ gh react 23
💬 GitHub PR Reaction Tool
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
👀 Fetching comments for PR #23...
👀 Repository: manishraj27/mern-project-cli
✅ PR #23 found!

👀 Gathering all comments and content...
✅ Found 3 items to react to!

📋 Available Content:
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[1] 💬 Comment by @manishraj27
    └─ test...

[2] 📄 PR Description by @manishraj27
    └─ fix: update homepage URL in package.json...

[3] 🔍 Code Review by @someuser
    └─ This looks good but consider...

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

😊 Choose what to react to:
🔢 Enter number (1-3): 1

👀 Selected: ISSUE by @manishraj27

😊 Available reactions:
  👍 +1       👎 -1       😄 laugh
  ❤️ heart    🎉 hooray   🚀 rocket   👀 eyes

🎯 Pick a reaction: +1

👀 Sending +1 reaction to comment...

🚀 Reaction added successfully! 🎉

🔗 View PR: https://github.com/manishraj27/mern-project-cli/pull/23
👍 Added thumbs up!
```

## User Experience

### 🎯 **Simple Number Selection**
No more copying long comment IDs! Just type `1`, `2`, or `3` to select what you want to react to.

### 🌈 **Beautiful Visual Interface**
- Color-coded content types (PR descriptions, comments, reviews)
- Progress indicators and status messages
- Emoji reactions and visual feedback
- Clean, organized layout with separators

### 💡 **Smart Error Handling**
- Validates PR existence before fetching
- Checks if you have proper access permissions
- Provides helpful tips when things go wrong
- Shows exact error details when needed

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

| Type | Icon | Description |
|------|------|-------------|
| **PR_BODY** | 📄 | The main PR description/body |
| **ISSUE** | 💬 | General comments on the PR conversation |
| **REVIEW** | 🔍 | Inline comments on specific lines of code |
| **REVIEW_SUMMARY** | 📝 | Comments submitted with code reviews |

## Requirements

- [GitHub CLI](https://cli.github.com/) installed and authenticated
- Access to the repository containing the PR
- Bash shell environment (Linux, macOS, WSL, Git Bash)

## Error Handling

The extension gracefully handles various scenarios:
- ❌ Invalid or non-existent PR numbers
- 🔒 PRs with no comments or restricted access
- 🔐 Authentication and permission issues
- 🌐 Network connectivity problems
- 🔢 Invalid number selections or reaction types
- 💡 Provides helpful tips and suggestions for resolution

## Quick Start

1. **Install the extension**:
   ```bash
   gh extension install manishraj27/gh-react
   ```

2. **Navigate to your repository**:
   ```bash
   cd your-repo
   ```

3. **React to a PR**:
   ```bash
   gh react 23
   ```

4. **Follow the prompts** - just type numbers and pick reactions!

## Contributing

1. Fork the repository
2. Create your feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License

MIT License - see LICENSE file for details.
