<!--
  This README is for the PUBLIC release repository (cove-dev/cove), which hosts
  download bundles and the updater manifest (latest.json) — not the source.
  Copy this file (and THIRD-PARTY-NOTICES.md) to that repo. Keep it download-
  and install-focused; build instructions belong in the source repo.
-->

# Cove

Local development environment manager for Windows. Install and run web servers,
databases, runtimes, and dev tools locally — versions, ports, HTTPS (local CA),
`hosts` entries, and per-site configuration from a single desktop app.

This repository hosts **release downloads** and the auto-update manifest for
Cove. The source is maintained separately.

## Download

Get the latest installer from the [**Releases**](../../releases/latest) page:

| File | Notes |
| --- | --- |
| `Cove_x.y.z_x64-setup.exe` | Recommended — installer, auto-updates |
| `Cove_x.y.z_x64-portable.exe` | Portable — single `.exe`, no install (update manually) |

**Requirements:** Windows 10 / 11, 64-bit (x64).

## Updating

Cove updates itself. Open **Settings → About → Check for updates** — new
versions are downloaded and installed from this repository's releases, then the
app restarts.

## Custom data location (`cove.ini`)

By default Cove stores everything under `%APPDATA%\Cove`. To choose where it
keeps its files — e.g. for a portable setup on another drive or a USB stick —
put a `cove.ini` file **next to the `.exe`**:

```ini
# Base folder: apps, tools, config, sites, logs, certs …  (default %APPDATA%\Cove)
home=D:\Cove

# Optional — data subtree only: databases & service data  (default <home>\data)
data=D:\Cove\data
```

- One `key=value` per line. `%VAR%` environment variables are expanded
  (e.g. `home=%USERPROFILE%\Cove`). Lines starting with `#` or `;` are comments.
- **Restart Cove** after editing `cove.ini` for changes to take effect.

## Third-party software

Cove downloads and runs developer tools (web servers, databases, runtimes, mail
catchers, and more) from their **official upstream sources** on demand. It does
not bundle or re-host them; each tool is governed by its own license. See
[THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).

## License

Cove is proprietary software. © 2026 burnz. All rights reserved.
