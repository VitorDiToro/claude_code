---
name: generating-commit-messages
description: Generates Conventional Commits (v1.0.0) compliant commit messages from git diffs. Use when writing commit messages or reviewing staged changes.
---

# Generating Commit Messages

## Instructions

1. Run `git diff --staged` to see changes
2. I'll suggest a commit message with:
   - **Summary under 50 characters**: Formatted strictly as `<type>[optional scope]: <description>`.
   - **Detailed description**: A body separated by a blank line, wrapped at 72 characters, explaining the context.
   - **Affected components**: Indicated clearly in the `[optional scope]` and further explained in the body or footer (along with issue references or BREAKING CHANGES).

## Allowed Types

- `feat`: A new feature
- `fix`: A bug fix
- `docs`: Documentation only changes
- `style`: Changes that do not affect the meaning of the code (white-space, formatting, etc)
- `refactor`: A code change that neither fixes a bug nor adds a feature
- `perf`: A code change that improves performance
- `test`: Adding missing tests or correcting existing tests
- `build`: Changes that affect the build system or external dependencies
- `ci`: Changes to our CI configuration files and scripts
- `chore`: Other changes that don't modify src or test files

## Best practices

- **Imperative mood:** Use present tense in the description (e.g., "add" instead of "added" or "adds").
- **Formatting:** Do not capitalize the first letter of the description and do not put a period (`.`) at the end.
- **Focus:** Explain *what* and *why* in the detailed description, not *how*.
- **Breaking Changes:** Append `!` after type/scope (e.g., `feat(api)!: `) or use `BREAKING CHANGE: ` in the footer.