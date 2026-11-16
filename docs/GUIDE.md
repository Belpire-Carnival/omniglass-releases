# OmniGlass Desktop guide (version 0.0.1)

## 1. Download and verify

1. Download `OmniGlass-Desktop-0.0.1-x64-setup.exe` from the [latest release](https://github.com/Belpire-Carnival/omniglass-releases/releases/latest).
2. Open a terminal (PowerShell or Command Prompt) in the folder where it was saved.
3. Run:

   ```
   certutil -hashfile OmniGlass-Desktop-0.0.1-x64-setup.exe SHA256
   ```

4. The hash must be exactly:

   ```
   cdfda69f8de43bb4c85af8f6f6a62b3a4dc41f5093befc64fd1006eac5e1685b
   ```

   If it differs, delete the file and download it again from this page. Do not run it.

## 2. Install

1. Double-click the installer.
2. If Windows SmartScreen says "Windows protected your PC", choose **More info**, then **Run anyway**. This appears because the installer is not code-signed yet.
3. Finish the setup. The app starts in the system tray (the icons near the clock; you may need to open the "hidden icons" arrow).

## 3. First run

1. Open **Settings** from the tray icon or the app window.
2. Check that the app can read your Star Citizen files. The Settings page reports this. If it cannot find the game, point it at your install folder (usually under `Roberts Space Industries\StarCitizen\LIVE`).
3. Start Star Citizen. The app follows your `Game.log` while you play.

If you have played before, Settings can also read your older logs, so blueprints you already own are recognised.

## 4. What is in the window

- **Overlay:** a click-through window over the game that shows events as they happen. It does not take mouse or keyboard input.
- **Blueprints:** which blueprints you own, and which you still need.
- **Reputation:** pick your rank on each ladder so contracts show whether you can take them.
- **Mining:** mining information from the game files.
- **Settings:** file checks, game data, older logs, and Field Notes.

## 5. Field Notes (optional, off by default)

Field Notes adds detail to the game's own text, so you see it inside the game's contract screens:

- **Blueprint marks:** contract titles show whether a reward blueprint is new to you or already owned.
- **Mission detail:** required rank, reputation gained, and the full list of blueprints a contract can reward, with owned or new.
- **Weapon stats:** damage per shot, rate of fire, DPS and magazine size for handheld weapons.
- **Reputation:** the reputation line in mission detail can be switched off separately.

Each part has its own switch in **Settings, Field Notes**.

### Turning it on

1. Close Star Citizen completely. The app refuses to write while the game is running.
2. In Settings, Field Notes, switch on the parts you want.
3. Press **Preview** to see what would change. Nothing is written yet.
4. Press **Apply**. The app saves your originals, writes `global.ini` for the English language, and makes sure `user.cfg` has `g_language = english`.
5. Start the game. The game must be restarted to pick up the change.

### Undoing it

Press **Roll back** in Settings, Field Notes. Your original files are restored exactly.

### After a game patch

A patch can change the game's text. Open Settings, Field Notes, and press Preview and Apply again so the notes match the new build.

### Good to know

- Field Notes only changes English text. Other game languages are not supported in 0.0.1.
- CIG allows community text files but does not endorse them. Use it if you are comfortable with that.
- If the game's text for a contract has no matching entry, that entry is skipped. Preview shows how many.

## 6. Troubleshooting

| Problem | What to try |
| --- | --- |
| SmartScreen blocks the installer | More info, then Run anyway. Check the SHA-256 first. |
| Hash does not match | Delete the file and download again from the releases page. |
| App cannot find the game | Set the install folder in Settings. Check you chose the right channel (LIVE or PTU). |
| No events appear | Start the game, then check that `Game.log` is being updated in the channel folder. |
| Field Notes will not apply | Make sure Star Citizen is fully closed. |
| Game text looks wrong after a patch | Press Roll back, then Preview and Apply again. |
| Something else is wrong | Open an issue with your version, channel and what happened. |

## 7. Uninstall

Use **Windows Settings, Apps, Installed apps**, find OmniGlass Desktop, and uninstall. If you used Field Notes, press **Roll back** first so your original game text files are restored.
