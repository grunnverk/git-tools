# @eldrforge/git-tools - Agentic Guide

## Purpose

Git utilities for automation. Provides secure process execution and comprehensive Git operations with validation and safety checks.

## Key Features

- **Secure Execution** - Safe shell command execution with input validation
- **Git Operations** - Comprehensive Git command wrappers
- **Input Validation** - Prevent command injection attacks
- **Error Handling** - Robust error handling and logging
- **No Dependencies** - Minimal footprint (only shell-escape and semver)

## Usage

```typescript
import { executeGitCommand, validateGitInput } from '@eldrforge/git-tools';

// Execute git command safely
const result = await executeGitCommand('status', ['--short']);

// Validate user input
const safeBranch = validateGitInput(userInput, 'branch-name');

// Get git information
const currentBranch = await getCurrentBranch();
const isDirty = await isWorkingTreeDirty();
```

## Dependencies

- shell-escape - Safe shell argument escaping
- semver - Semantic version parsing

## Package Structure

```
src/
├── child.ts         # Child process execution
├── git.ts           # Git command wrappers
├── validation.ts    # Input validation
├── logger.ts        # Logging utilities
└── index.ts
```

## Key Exports

- `executeGitCommand()` - Execute git commands safely
- `executeCommand()` - Execute arbitrary commands safely
- `validateGitInput()` - Validate git-related input
- `getCurrentBranch()` - Get current git branch
- `isWorkingTreeDirty()` - Check for uncommitted changes
- `getRemoteUrl()` - Get remote repository URL
- `getBranchCommits()` - Get commits on branch

