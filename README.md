# Fyug

This repository holds releases of the Fyug app: the `fyug` command line and
the `fyug-mcp` server. Download them from
[Releases](https://github.com/Ilusiv-media/fyug/releases).

## Install

macOS (Apple silicon) and Linux (x86_64, arm64):

```sh
curl -fsSL https://github.com/Ilusiv-media/fyug/releases/latest/download/install.sh | sh
```

Windows (x86_64), in PowerShell:

```powershell
powershell -ExecutionPolicy ByPass -c "irm https://github.com/Ilusiv-media/fyug/releases/latest/download/install.ps1 | iex"
```

The installer checks each download against the release's `SHA256SUMS.txt` and
installs nothing if a checksum is missing or doesn't match.
