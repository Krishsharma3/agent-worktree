# agent-worktree (local copy)

This folder contains a local copy / helper README for the upstream `agent-worktree` project (https://github.com/nekocode/agent-worktree).

## Purpose
- Provide a separate local repo folder you can push to your own GitHub.
- Summarize install and quick-use commands.

## Options
1) Use the upstream repo directly (recommended):

```bash
# clone upstream into this folder
git clone https://github.com/nekocode/agent-worktree.git .
```

2) Create a fresh local repo and push this copy to your own GitHub:

```bash
# from inside agent-worktree/ (this folder)
git init
git add .
git commit -m "Initial import of agent-worktree notes"
# create a GitHub repo first, then add its remote:
git remote add origin git@github.com:<your-username>/agent-worktree.git
git branch -M main
git push -u origin main
```

## Install
The project provides an npm CLI `wt` (agent-worktree). Install globally:

```bash
npm install -g agent-worktree
# or use pnpm:
pnpm add -g agent-worktree
```

Reinstall shell integration or setup manually:

```bash
wt setup    # installs shell integration for bash/zsh/fish/PowerShell
```

## Quick Start

```bash
# create a new isolated worktree and enter it
wt new
# or create with a branch name
wt new feature-x

# enter (or switch)
wt cd feature-x

# after work, merge back to trunk and cleanup
wt merge
```

Snap mode (agent workflows):

```bash
# create + run agent in snap mode
wt new -s "aider --model sonnet"
# or
wt new -s claude
```

## Useful commands

- `wt ls` — list worktrees
- `wt cd <name>` — switch to a worktree
- `wt main` — return to main repo
- `wt merge` — merge worktree back to trunk
- `wt rm <name>` — remove worktree
- `wt clean` — remove unchanged worktrees

## Project config
Project-specific config can be in `.agent-worktree.toml` (see upstream for details). Global config at `~/.agent-worktree/config.toml`.

## Upstream
Full docs and examples are at: https://github.com/nekocode/agent-worktree

---

If you want, I can now clone the upstream repo into this folder, or initialize a fresh git repo and push to your GitHub. Which would you like me to do?