# FlowQ Connect

Official download page for **FlowQ Connect**, the desktop agent for Infinity Flow Cloud.

FlowQ Connect runs on a computer on your network and acts as a **secure bridge** between your **printers** and **Infinity Flow Cloud**—so jobs and device state can move between your shop floor and the cloud without exposing printers directly to the internet.

This repository hosts **versioned binaries and installers only**. Source code is not published here.

---

## What you get

Each [GitHub Release](https://github.com/infinity-flow-3d/flowq-connect-releases/releases) includes:

| Asset | Description |
|--------|-------------|
| **FlowQ Connect (desktop)** | Application bundles: **macOS** (`.dmg`), **Windows** (installer `.exe`), **Linux** (`.deb`). The app provides a compact UI for **starting and stopping** the agent and for **pairing or relinking** it to your account. |
| **`flowq-agent` (CLI)** | Standalone binaries for scripting and headless use: `flowq-agent-macos-arm64`, `flowq-agent-linux-amd64`, `flowq-agent-linux-arm64`, `flowq-agent-windows-amd64.exe`. |
| **`install.sh`** | Optional installer for the **macOS/Linux** CLI: installs to `~/.flowq/bin`, updates `PATH` when needed, and runs `flowq-agent install`. |

In many setups, FlowQ Connect **replaces the earlier ESP32-based FlowQ Hub**—one desktop agent instead of extra network hardware.

---

## System requirements

- **macOS** — Apple Silicon (`arm64`) for the artifacts produced by the current release workflow; use the `.dmg` or `flowq-agent-macos-arm64`.
- **Linux** — `x86_64` or `arm64` (CLI naming as above).
- **Windows** — `x86_64` — use the NSIS installer or `flowq-agent-windows-amd64.exe`.

You need reliable connectivity from the host machine to **Infinity Flow Cloud**. Supported printers and cloud features depend on your Infinity Flow plan and configuration.

---

## Installation

### Desktop app (typical)

1. Open [**Releases**](https://github.com/OWNER/REPO/releases/latest).
2. Download the **macOS** `.dmg`, **Windows** `.exe`, or **Linux** `.deb`.
3. Install and open **FlowQ Connect**, then complete pairing when prompted.

### CLI — install script (macOS / Linux)

Point `install.sh`’s `BASE_URL` at **this** repository’s latest-download URLs, then:

```bash
curl -fsSL https://github.com/OWNER/REPO/releases/latest/download/install.sh | bash
