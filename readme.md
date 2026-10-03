# Hermaion Companion

The desktop companion for members of **Hermaion Corporation**. A small Windows tray app that connects Star Citizen to Hermaion HQ ([hermaion.eu](https://hermaion.eu)), so the paperwork happens while you fly.

Everything it does is also on the website. The app adds hotkeys, reading your wallet or a contract off the screen, pausing your run when the game closes, and your position for an SOS.

## Download

Get the latest installer from **[Releases](../../releases/latest)**: the file ending in `-setup.exe`. Windows 10 or 11, 64-bit.

It installs for your Windows user only, without admin rights, and updates itself after that.

## Install and connect (5 minutes)

1. **Run the installer.** Windows may say it protected your PC, because the installer is not signed with a paid certificate. Choose **More info**, then **Run anyway**.
2. **Make a token on HQ.** Sign in at [hermaion.eu](https://hermaion.eu), open **Profile**, then **Desktop companion**, and choose **Create token**. It is shown once: copy it.
3. **Paste it into the app.** The app opens its Settings window on first start (later: right-click the tray icon, **Settings**). Paste the token and choose **Save and connect**. The tray menu now shows your active contract.

Lost your PC or token? Revoke the token on your HQ profile; the app stops working at once.

## Hotkeys

They work while Star Citizen runs in **borderless windowed** mode. Change them in Settings.

| Hotkey | What it does |
|---|---|
| **Ctrl+Alt+N** | Moves your active contract to its next stage (Loading, Awaiting clearance, In transit, Unloading, Delivered), exactly as the Dispatch page would. |
| **Ctrl+Alt+W** | Reads your aUEC balance from the screen and updates it on HQ. Open the mobiGlas home or wallet first. |
| **Ctrl+Alt+C** | Reads the contract open in your mobiGlas and sends it to HQ as a draft. Check it on Dispatch and post it with one click. |
| **Ctrl+Alt+I** | Interdicted: logs it on your active run and warns everyone of the spot on HQ's Hazards page and in the planners. |
| **Ctrl+Alt+S, twice** | **SOS**, for critical danger. Press twice within 3 seconds (the first press only gets it ready). Your call goes up on HQ and in #sos-beacon with your ship, your run and your last position from the game's log. Press again later to update it. |

## The tray menu

Right-click the Hermaion icon by the clock:

- Your active contract and its next step, or **Back in game** while it is on hold.
- **Game crashed**, **Interdicted**, **Ask for an escort**, **Send SOS** (or **I am safe** while one is out).
- **Read wallet from screen**, **Read contract from screen**.
- Your balance and payouts on HQ.
- **Open in HQ**: SOS, Run planner, Hazards, Escorts, Payouts, Price alerts.
- **Settings**, **Refresh**, and **Install version** when an update is ready.

Desktop notifications confirm every action, and pop up for price alerts, escorts taken on your runs, members' SOS calls and members answering yours.

## When the game closes mid-run

On by default (Settings, "Pause my run when Star Citizen closes"). When Star Citizen closes during a run, a crash or calling it a night, your run goes on hold: the countdown on your contract card stops. When the game is back, the run resumes and its arrival moves back by the time lost.

## Your SOS position

When you send an SOS, the app reads the game's own text log (`Game.log` in the game's `LIVE` folder) and picks out the lines that say where you are: arriving at a station, choosing and finishing a quantum jump, entering a planet's space, going down. HQ turns those into "Area18, ArcCorp" or "Quantum travel from Orbit of Hurston to Orison, Crusader".

Game installed somewhere other than `C:\Program Files\Roberts Space Industries\StarCitizen\LIVE`? Set the path to `Game.log` in Settings.

The game does not document these lines and can change them with a patch, so this is best effort: with nothing found, the SOS goes out with your run instead.

## Safe with Easy Anti-Cheat

The app **never reads the game's memory, never injects anything and never touches the game's process**. It only:

- sees the screen when you press a hotkey, like taking a screenshot;
- sees the game's name in Windows' list of running programs, the way Discord shows which game you play;
- reads the game's own text log when you send an SOS, the way Notepad would.

## What is sent, and what is not

- **Sent to HQ:** your balance, a contract's text or a stage change when you press a hotkey; for an SOS, the kind of event, the place code and its time.
- **Never sent:** screenshots (read on your PC and thrown away), your log file (only the few lines that place you, reduced to a code and a time), your PC's name or Windows user name.
- **Your token** is kept in Windows Credential Manager, not in a file.
- **Crash reports** (when the app itself fails) go to the Board's error tracker with tokens, screen text, balances and machine and user names removed.

## Updates

The app checks for updates and offers **Install version** in the tray menu. Every update is signed by Hermaion; the app refuses any update that is not.

## Uninstall

Windows **Settings**, **Apps**, **Installed apps**, **Hermaion Companion**, **Uninstall**. Then revoke its token on your HQ profile.

## Trouble?

| Problem | Try |
|---|---|
| "HQ did not accept the token" | Make a new token on your profile and paste it in Settings. |
| A hotkey does nothing | Run the game in borderless windowed mode. If Settings says a key is taken by another program, pick another combination. |
| The wallet is not read | Open the mobiGlas home or wallet so the aUEC figure is on screen, then press the hotkey. |
| The SOS has no position | Check the `Game.log` path in Settings. Right after you spawn, the log may not place you yet. |
| Windows blocks the installer | **More info**, then **Run anyway**. |

Anything else: ask in the Hermaion Discord.

---

Hermaion Corporation. Secure transport. Complete discretion. Every route, a windfall.
