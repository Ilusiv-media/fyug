# Fyug

Fyug lets you and your AI agent compose generative music together and hear it play live as you change it.

## Install

macOS (Apple silicon) and Linux with glibc (x86_64, arm64):

```sh
curl -fsSL https://github.com/Ilusiv-media/fyug/releases/latest/download/install.sh | sh
```

Windows (x86_64), in PowerShell:

```powershell
powershell -ExecutionPolicy ByPass -c "irm https://github.com/Ilusiv-media/fyug/releases/latest/download/install.ps1 | iex"
```

## Add Fyug to Claude Code and Codex

Register the Fyug MCP server with the agents on this machine:

```sh
fyug setup
```

`fyug setup` finds Claude Code, Codex (including the ChatGPT desktop app),
Claude Desktop and Cursor, and adds the `fyug-mcp` server to each one's MCP
configuration. Run `fyug setup --print` to see the exact changes without
writing them. Restart the agent, then ask it to compose something.

## About the install

The installer checks each download against the release's `SHA256SUMS.txt` and
installs nothing if a checksum is missing or doesn't match. It puts `fyug` and
`fyug-mcp` in `~/.fugue/bin` and tells you if that folder is not on your
`PATH`.

Other ways to install, from the same release:

- **Claude Desktop:** download the `.mcpb` bundle for your platform from the
  [latest release](https://github.com/Ilusiv-media/fyug/releases/latest) and
  open it. It carries its own `fyug` and `fyug-mcp`.
- **Homebrew:** `brew install gdamron/tap/fyug`.
- **macOS app:** the `.dmg` on the latest release holds `Fugue.app`.

## About this repository

This repository holds releases of the Fyug app: the `fyug` command line and
audio engine, and the `fyug-mcp` server. Download them from
[Releases](https://github.com/Ilusiv-media/fyug/releases). Fyug is built on the
open-source [Fugue](https://github.com/gdamron/fugue) engine.
