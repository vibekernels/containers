# agent-containers
Collection of custom containers for coding agents.

## Images

| Image | Base | Target Hardware |
|-------|------|-----------------|
| `x64-claude` | Ubuntu 24.04 | General-purpose x64 (e.g. AWS T3) |
| `cuda-claude` | NVIDIA CUDA 12.8.1 / Ubuntu 24.04 | NVIDIA GPU instances |
| `tt-metal-claude` | Tenstorrent tt-metal / Ubuntu 22.04 | Tenstorrent accelerators |

All images are published to `ghcr.io/vibekernels/agent-containers/<image>:latest`.

## Environment Variables

| Variable | Description | Default |
|----------|-------------|---------|
| `CLAUDE_PROMPT` | Initial prompt sent to Claude Code on startup | _(none)_ |
| `CLAUDE_MODEL` | Model to use | `opus` |
| `CLAUDE_EFFORT` | Effort level (`high`, `medium`, `low`) | `high` |
| `CLAUDE_CODE_OAUTH_TOKEN` | OAuth token for authenticating Claude Code | _(none)_ |
| `PUBLIC_KEY` | SSH public key injected into the container for access | _(none)_ |
