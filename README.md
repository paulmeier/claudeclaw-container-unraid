# claudeclaw-container-unraid

[![Lint](https://github.com/paulmeier/claudeclaw-container-unraid/actions/workflows/lint.yml/badge.svg)](https://github.com/paulmeier/claudeclaw-container-unraid/actions/workflows/lint.yml)
[![CI](https://github.com/paulmeier/claudeclaw-container-unraid/actions/workflows/ci.yml/badge.svg)](https://github.com/paulmeier/claudeclaw-container-unraid/actions/workflows/ci.yml)
[![Release](https://img.shields.io/github/v/release/paulmeier/claudeclaw-container-unraid)](https://github.com/paulmeier/claudeclaw-container-unraid/releases)

Unraid Community Applications template for [claudeclaw-container](https://github.com/paulmeier/claudeclaw-container) — a Docker container running [claudeclaw](https://github.com/moazbuilds/claudeclaw) as a persistent Claude Code personal assistant daemon.

## Template

- **Docker image**: `paulmeier/claudeclaw-container:latest`
- **Project**: https://github.com/paulmeier/claudeclaw-container
- **Docker Hub**: https://hub.docker.com/r/paulmeier/claudeclaw-container

## Installation

### Via Community Applications (recommended)

Search for **claudeclaw** in the Unraid Apps tab.

To add this repository as a template source manually:

1. In Unraid, open the **Apps** tab and go to **Settings**.
2. Under **Template Repositories**, add:
   ```
   https://github.com/paulmeier/claudeclaw-container-unraid
   ```
3. Click **Check for Updates**, then search for **claudeclaw**.

### Manual installation

1. In Unraid, go to **Docker** → **Add Container**.
2. Click **Load template from URL** and paste:
   ```
   https://raw.githubusercontent.com/paulmeier/claudeclaw-container-unraid/main/templates/claudeclaw-container.xml
   ```
3. Click **Load**, fill in any required fields, and click **Apply**.

## First-run authentication

claudeclaw uses your Claude Code subscription — no API key needed. After the container starts for the first time, open a terminal to it and run:

```bash
claude login
```

This opens an OAuth browser flow. Complete it once and credentials are saved permanently in the app data volume.

## Configuration

Edit `settings.json` in your app data directory (`/mnt/user/appdata/claudeclaw/claudeclaw/settings.json`) to configure messaging bridges and other options. Use [settings.example.json](https://github.com/paulmeier/claudeclaw-container/blob/main/settings.example.json) as a starting point.

## Support

Open an issue: https://github.com/paulmeier/claudeclaw-container-unraid/issues
