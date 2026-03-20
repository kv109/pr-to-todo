# pr-to-todo

Generate a self-contained HTML TODO app from GitHub PR review comments. Each review thread becomes a checkbox item you can mark as resolved, with state saved in your browser's localStorage.

## Requirements

- [GitHub CLI (`gh`)](https://cli.github.com/) — authenticated with access to the target repo
- Python 3
- Bash

## Usage

```sh
./prtodo <github-pr-url>
```

Example:

```sh
./prtodo https://github.com/owner/repo/pull/123
```

This generates `output/pr-123-todos.html`. Open it in your browser.

## Features

- Threads grouped by file path and position in diff
- Colorized diff context for each thread
- Checkbox to mark threads as resolved (persisted in localStorage)
- Yellow "resolved" label for threads already resolved on GitHub
- Filter by status (all / unresolved / resolved)
- Filter by author (include / exclude, multiselect)
- File paths link to the PR's Files tab on GitHub
- Comment info links to the original comment on GitHub
- Copy file path to clipboard
