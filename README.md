# SCUM - MCP (THIS IS A WORK IN PROGRESS AND NOT ALL OPTIONS ARE EVEN OPERATIONAL YET)

A Windows desktop app for running SCUM: your game client, your dedicated server and the mods for both, all in one place.

It runs **fully offline**. No account, no internet and no AI are needed. The only things that go online (game updates through SteamCMD, and the optional app update check) happen when you press their button.

**[Download the latest version](https://github.com/DrSmith879/SCUM---MCP---Releases/releases/latest)**: pick `Scum - MCP - v<version> (Windows).zip`.

---

## Features

### ADMIN
- **Client Panel**: launch SCUM in two ways.
  - **Vanilla** starts through Steam with BattlEye on and client mods switched off.
  - **Modded** starts SCUM.exe directly with `-fileopenlog -nobattleye`, so UE4SS mods load.
  - It also installs, removes and backs up the client's `.pak` mods.
- **Server Panel** (preinstalled module): manage a dedicated server on this PC.
  - Start, Restart, safe Stop (the server saves first), Force stop, Backup now and Validate files.
  - Vitals: status, players, CPU, memory and uptime.
  - Operations: next restart (or skip it), backups and crash recovery.
  - World settings from ServerSettings.ini and counts from the last save.
  - Server history chart, live server log, players online, chat and recent activity.
  - Daily restart schedule, automatic world backups with restore, and crash recovery.

### Bundled mods
| Mod | Runs on | What it does |
|---|---|---|
| Population Controller | Server (Client for single-player) | Controls zombie, NPC, animal and drone numbers and spawn distances, with calculators and a live spawn diagram |
| Wilderness NPC pak | Server (Client for single-player) | Adds armed NPC encounters to the wilderness |
| Developer Mode | Server (Client for single-player) | Admin tiers and developer access, with its own manager |
| Crosshair | Client only | A crosshair that stays on screen after reconnects, with 12 styles and colours |

### Mod Manager
- Shows where every mod folder is and whether it was found.
- Installs the official UE4SS v4.0.0 from a ZIP you downloaded.
- Each mod installs to the **Client**, the **Server** or **Both**:
  - client-side UI mods are locked to Client;
  - server mods default to Server.
- Switches for UE4SS mods, a `.pak` mod list, and add-ons / plugins.

### Settings
- General and Startup options.
- Game directories.
- Modules: remove or reinstall any module.
- Game updates through SteamCMD.
- App updates, logs and snapshots, compatibility, and license.

---

## Install

1. Download `Scum - MCP - v<version> (Windows).zip` from [Releases](https://github.com/DrSmith879/SCUM---MCP---Releases/releases/latest).
2. Extract it to a folder you can write to, for example `C:\SCUM\SCUM-MCP\`. Keep all the files together.
3. Run `SCUM-MCP.exe` and accept the license on the first run.
4. Go to **Settings > Game Directories** and set your SCUM Client folder, your Server folder or both. Then press **Save & Apply**.

Requires Windows 10 or 11, 64-bit. No .NET install is needed.

## Updating

Go to **Settings > App Updates > Check for updates**.
- The app downloads only the parts that changed. A typical update is under 1 MB.
- Every file is checked against a signed release list before it is used.
- The files it replaces are backed up, and **Roll back** puts them back.
- The startup update check is **Off** by default.
- With no internet, you can download a release's files by hand and use **Install from a downloaded release folder**.

## Safety

- Nothing is changed while the server or game it affects is running.
- Every file is copied to `%LOCALAPPDATA%\SCUM-MCP\Backups\` before it is changed or removed.
- Updating a mod never overwrites your `.ini` or config settings.

## Files and logs

- App settings and log: `%LOCALAPPDATA%\SCUM-MCP\` (`settings.json`, `Logs\app.log`).
- If something goes wrong, include `app.log` when you report it.

## Release files (for each version)

| File | Purpose |
|---|---|
| `Scum - MCP - v<version> (Windows).zip` | Full download for new installs |
| `updates.json`, `updates.json.sig` | Signed list the app uses to update |
| `scum-mcp-app.zip`, `scum-mcp-runtime.zip`, `scum-mcp-payload.zip` | The parts the in-app updater downloads |

---

## License

Copyright (c) 2026 Whiteleyj. All rights reserved. SCUM - MCP is proprietary software; see `LICENSE.txt` in the download. Third-party components keep their own licenses (see `THIRD-PARTY-NOTICES.txt`).

SCUM is a trademark of its respective owners. This project is not affiliated with or endorsed by the developers or publishers of SCUM.
