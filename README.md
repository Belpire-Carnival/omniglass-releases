# OmniGlass Desktop

A Windows tray app that reads Star Citizen's own log files and shows you what is happening: events, blueprints you own, reputation, and mining, with an in-game overlay of cards you can move and resize. It is part of the OmniOps companion at <https://bureau.belpire.com/rsi1/companion/>.

**Current version: 0.1.0**

## Download

[OmniGlass-Desktop-0.1.0-x64-setup.exe](https://github.com/Belpire-Carnival/omniglass-releases/releases/latest/download/OmniGlass-Desktop-0.1.0-x64-setup.exe)

SHA-256: `1c0399451758ced43368831a1895a31fa990ea73606e73c7a3da639b751f09a2`

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
