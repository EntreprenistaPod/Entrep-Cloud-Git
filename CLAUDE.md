# Entreprenista Podcast Automation

## Project Context

The user is automating pieces of the podcast workflow for **Entreprenista**. The end goal is to create Claude routines that execute on a scheduled basis inside Claude Code.

The user works in the **Claude Code desktop app** and is **non-technical** — all guidance must be clear, step-by-step, and jargon-free.

## Skills

This project is built around **skills** — reusable Claude commands stored as `.md` files in the `commands/` folder. Each skill becomes a slash command (e.g. `/skill-name`) you can run in any Claude Code session.

### How to create a skill

1. Create a new `.md` file in the `commands/` folder (e.g. `show-notes.md`)
2. Give it a clear `# Title` and a description of what it does
3. Write the instructions Claude should follow under a `## Prompt` section
4. Use `$ARGUMENTS` anywhere you want to pass in dynamic input (like an episode title)
5. Save the file — Claude will automatically commit and sync it to GitHub

### Skill file template

```markdown
# skill-name

One sentence describing what this skill does.

## Prompt

$ARGUMENTS

Step-by-step instructions for Claude to follow...
```

## Session Rules (Claude must follow these every session)

- **On session start:** check that the local repo is on the `main` branch and in sync with the remote. If not, pull and switch to `main` before doing anything else.
- **After every skill is created or edited:** automatically commit the change with a clear message and push to `origin main`.
- **Never commit to any branch other than `main`.**
- **You (Claude) are responsible for all git operations** — the user should never need to run git commands manually.

## Workflow: Creating a New Scheduled Routine

1. Work with the user to define what the routine should do
2. Create the skill `.md` file in the `commands/` folder
3. Commit and push to the remote automatically
4. Guide the user to set up the schedule using `/schedule` in Claude Code

## Remote Repo

- **GitHub:** https://github.com/EntreprenistaPod/Entrep-Cloud-Git
- **Branch:** `main`
