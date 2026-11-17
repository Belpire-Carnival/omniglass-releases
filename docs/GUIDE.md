# OmniGlass Desktop guide (version 0.1.0)

## 1. Download and verify

1. Download `OmniGlass-Desktop-0.1.0-x64-setup.exe` from the [latest release](https://github.com/Belpire-Carnival/omniglass-releases/releases/latest).
2. Open a terminal (PowerShell or Command Prompt) in the folder where it was saved.
3. Run:

   ```
   certutil -hashfile OmniGlass-Desktop-0.1.0-x64-setup.exe SHA256
   ```

4. The hash must be exactly:

   ```
   1c0399451758ced43368831a1895a31fa990ea73606e73c7a3da639b751f09a2
   ```

   If it differs, delete the file and download it again from this page. Do not run it.

## 2. Install

1. Double-click the installer.
2. If Windows SmartScreen says "Windows protected your PC", choose **More info**, then **Run anyway**. This appears because the installer is not code-signed yet.
3. Finish the setup. The app starts in the system tray (the icons near the clock; you may need to open the "hidden icons" arrow).

## 3. First run

1. Open the app window. Left-click the tray icon to bring it back if it is hidden.
2. Check that the `Game.log` line shows your install (for example the LIVE folder). If not, type the path to your `Game.log` and press **Use this file**. It is usually under `Roberts Space Industries\StarCitizen\LIVE`.
3. Under **Game data** in Settings, pick LIVE or PTU and press **Check for updates** once.
4. Start Star Citizen. The app follows your `Game.log` while you play.

If you have played before, Settings can also read your older logs, so blueprints you already own are recognised.

## 4. What is in the window

- **Events:** what the log shows, with a filter and a copy-as-text button.
- **Blueprints:** which blueprints you own, and which you still need.
- **Minerals:** search an ore, see its compositions and where it spawns.
- **Reputation:** pick your rank on each ladder so contracts show whether you can take them.
- **Settings:** file checks, game data, older logs, in-game timers, the website connection, and Field Notes.
- **Overlay:** a click-through window over the game made of cards you can move and resize (see sections 5 and 6).

## 5. Hotkeys

| Keys | What it does |
| --- | --- |
| `Ctrl+Shift+O` | Open or close the overlay drawer (the Recent, Watching and This session cards). Alerts and running timers show even when it is closed. |
| `Ctrl+Shift+F` | Search a blueprint or mineral. Type, press **Enter** to pin the top result to Watching, **Esc** (or the hotkey again) to close. Clicking another program also closes it. The keyboard goes back to the game. |
| `Ctrl+Shift+E` | Move and resize the overlay cards. **Esc**, **Done** or the hotkey again saves and finishes. |

- The hotkeys work while the app is running, even with the game in front. They cannot be changed yet.
- If another program already holds a hotkey, the app starts without it and everything else still works.
- The overlay only shows over the game in **borderless windowed** mode, not exclusive fullscreen.

## 6. Overlay cards

The overlay is made of cards: **Recent** events, your **Watching** list, **This session**, **Timers**, and pop-up **Alerts**.

1. Press `Ctrl+Shift+O` to open the drawer.
2. Press `Ctrl+Shift+E`. The screen dims and a bar appears.
3. Drag a card to move it. Drag its bottom-right corner to resize it. Tick or untick a card in the bar to show or hide it.
4. There are two saved layouts, **Flying** and **On foot**. Choose one in the bar before you arrange; you switch between them by hand. **Reset layout** puts the current one back to the default.
5. Press **Done**. Positions are kept on this PC as a share of your screen, so they survive a change of resolution.

Dragging only moves the app's own window. Nothing is sent to the game.

## 7. Timers, the session card and the website connection

**Timers.** In Settings, In-game timers, type a label such as `Refinery Pyro` and a time such as `2h 10m`, `45m` or `1:30:00` (up to 7 days, eight at once), then press **Start**. The Timers card counts down on the overlay and posts a **Timer done** alert when it ends. The game does not write refinery jobs to its log, so a timer runs on the time you type. Timers survive restarting the app.

**This session.** Counts what the log shows since the game started: contracts accepted, missions completed, blueprints received, ships destroyed and lost, and times you went down. The clock stops when the game closes.

**Show your live game data on the website.**

1. In Settings, tick **Let the website connect**. The app shows an 8-character code and copies it.
2. On <https://bureau.belpire.com/rsi1/companion/> open OmniOps, find the **From your game** card, type the code and press **Connect**.
3. Use **Disconnect** at the bottom of that card to stop. **New code** in the app cuts off anything already connected, and unticking the switch turns it off.

The connection stays on your own PC (127.0.0.1) and only accepts that website.

## 8. Field Notes (optional, off by default)

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

### Naming

Under Settings, Field Notes you can rename the label on added lines and the two blueprint tags. Press Preview or Apply to put a new name into the game.

### After a game patch

A patch can change the game's text. Open Settings, Field Notes, and press Preview and Apply again so the notes match the new build.

### Good to know

- Field Notes only changes English text. Other game languages are not supported in 0.1.0.
- CIG allows community text files but does not endorse them. Use it if you are comfortable with that.
- If the game's text for a contract has no matching entry, that entry is skipped. Preview shows how many.

## 9. Troubleshooting

| Problem | What to try |
| --- | --- |
| SmartScreen blocks the installer | More info, then Run anyway. Check the SHA-256 first. |
| Hash does not match | Delete the file and download again from the releases page. |
| App cannot find the game | Set the install folder in Settings. Check you chose the right channel (LIVE or PTU). |
| No events appear | Start the game, then check that `Game.log` is being updated in the channel folder. |
| No overlay over the game | Switch the game to borderless windowed mode. |
| A card is off screen after changing monitors | Press `Ctrl+Shift+E`, then **Reset layout**. |
| Field Notes will not apply | Make sure Star Citizen is fully closed. |
| Game text looks wrong after a patch | Press Roll back, then Preview and Apply again. |
| Something else is wrong | Open an issue with your version, channel and what happened. |

## 10. Uninstall

Use **Windows Settings, Apps, Installed apps**, find OmniGlass Desktop, and uninstall. If you used Field Notes, press **Roll back** first so your original game text files are restored.
