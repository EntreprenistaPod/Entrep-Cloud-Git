# Claude Commands

This folder contains custom slash commands for Claude Code.

## Usage

Place `.md` files in this directory to create project-level slash commands.
Each file becomes a `/command-name` you can invoke in Claude Code sessions.

## Structure

```
commands/
├── CLAUDE.md          # This file
└── your-command.md    # Becomes /your-command
```

## Writing a Command

Each command file should include:

- **Purpose** — what the command does
- **Prompt** — the instructions Claude will follow
- **Optional args** — how to pass arguments via `$ARGUMENTS`

### Example

```markdown
# my-command

Does something useful.

## Prompt

$ARGUMENTS

Your instructions here...
```

## References

- [Claude Code slash commands docs](https://docs.anthropic.com/en/docs/claude-code/slash-commands)
