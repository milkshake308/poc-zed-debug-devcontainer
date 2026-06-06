## Step to Repro
- 1. Open this project in devcontainer
- 2. Launch `Launch main.py` or `Launch main.js`
- 3. You'll see the same `error: Connection to TCP DAP timeout 127.0.0.1:******`

`Launch main.go` is intentionally kept as a counterexample

## Works with SSH
If you reopen this project via Zed's SSH session into this container as the
ubuntu user, you should be able to launch the Python and JavaScript debuggers without issue.
