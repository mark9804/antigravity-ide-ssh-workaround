---
trigger: always_on
glob:
description:
---

# Remote Development Environment

This project is developed locally on macOS but **executed and debugged on a remote Linux server**.

## Connection Details

- **SSH Host Alias**: `[Alias]`
- **Hostname**: `[Hostname]`
- **User**: `[User]`
- **Port**: `[Port]`
- **Auth**: Public key (no password required)
- **Local Project Path**: `[Local Path]`
- **Remote Project Path**: `[Remote Path]`

## Rules for the Agent

1. **Code editing** happens locally. Write and modify files on the local filesystem as usual.
2. **Running training scripts, debugging, and any GPU-dependent tasks** must be executed on the remote server via SSH.
3. When the user asks you to "run", "debug", or "test" a script, default to running it on the remote server unless explicitly told otherwise.
4. **Use the `sh remote-execute <command>` script** for most remote commands. This script automatically syncs local code to the remote server and executes your command in the correct remote directory (`[Remote Path]`). For example: `sh remote-execute uv run test.py`.
5. For interactive or long-running commands that cannot be handled by `remote-execute`, use `ssh -t [Alias] '<command>'`. If using plain SSH, remember to always `cd [Remote Path]` first.
