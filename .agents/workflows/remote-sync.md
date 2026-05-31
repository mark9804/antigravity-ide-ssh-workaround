---
description: Sync local code to the remote server and run commands remotely
---

# Sync Local Code to Remote Server

// turbo-all

## Using remote-execute

1. The project provides a `remote-execute` script that automatically syncs code and runs the command remotely. You should use it directly:

```bash
./remote-execute <COMMAND>
```

Replace `<COMMAND>` with the actual command to run (e.g., `uv run test.py`, `nvidia-smi`, etc.).
This script handles the `rsync` with appropriate exclusions and the `ssh` execution for you.
