---
description: Debug a script on the remote server
---

# Debug on Remote Server

// turbo-all

## Steps

1. Use the `remote-execute` script to sync your code and run the script with necessary debug flags:

```bash
./remote-execute <DEBUG_COMMAND>
```

- If you need to check GPU status:

```bash
ssh <Alias> 'nvidia-smi'
```

_(Or use `bash remote-execute nvidia-smi` which will also sync before running)_

- If you need to check running processes:

```bash
ssh <Alias> 'ps aux | grep python'
```

- If you need to inspect remote logs or files:

```bash
ssh <Alias> 'cat <REMOTE_PATH>/<LOG_FILE>'
```
