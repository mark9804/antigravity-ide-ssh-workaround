# Antigravity-IDE-SSH-Workaround

This template repository serves as a temporary workaround for the issue that Antigravity IDE 2.0 breaks normal SSH connection function. The fix is to force Antigravity IDE to use the project's remote-sync script instead of its built-in SSH extension.

## How to use

0. Go to [Google AI forum](https://discuss.ai.google.dev/c/antigravity/), create a post and report this sh*t.
1. Clone this repo as a project template.
2. In `remote-sync`, update the `REMOTE_DIR` and `ALIAS` variables to match your remote server.
3. In `.agents/rules/remote-dev.md`, update placeholder variables to match your remote server.
4. Happy(?) remote developing!
