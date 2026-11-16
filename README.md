# OmniGlass Desktop

A Windows tray app that reads Star Citizen's own log files and shows you what is happening: events, blueprints you own, reputation, and mining. It is part of the OmniOps companion at <https://bureau.belpire.com/rsi1/companion/>.

**Current version: 0.0.2**

## Download

[OmniGlass-Desktop-0.0.2-x64-setup.exe](https://github.com/Belpire-Carnival/omniglass-releases/releases/latest/download/OmniGlass-Desktop-0.0.2-x64-setup.exe)

SHA-256: `7a7eea12109c24c3e67d44f4924e539fe457b48572d029ed6cf36f2769ffbd9d`

Only install it from this page or from the companion site. Do not install copies from other places.

## Requirements

- Windows 10 or 11, 64-bit
- Star Citizen installed on the same PC

## The installer is not code-signed

Windows SmartScreen will warn that the publisher is unknown. This is expected for an unsigned installer. Check the SHA-256 first (see the guide), then choose **More info**, then **Run anyway**.

## What it does and does not do

- **Never:** reads game memory, injects code, or sends keystrokes or mouse input.
- **Reads, read-only:** your `Game.log`, your archived logs, and the game's own data file (`Data.p4k`).
- **Writes game files only if you switch on Field Notes.** It is off until you do. Applying it writes the game's English text file (`global.ini`) and makes sure `user.cfg` selects English, after saving your originals. **Roll back** restores them exactly. It will not write while the game is running.

## Guide

Step-by-step install, verification, first run, Field Notes and troubleshooting: [docs/GUIDE.md](docs/GUIDE.md)

## Feedback

Open an issue in this repository. Say which version you ran, your Star Citizen channel (LIVE or PTU), and what you expected to happen.
