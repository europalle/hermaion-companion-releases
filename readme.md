# Hermaion Companion

The desktop companion for members of **Hermaion Corporation**. A small Windows tray app that connects Star Citizen to Hermaion HQ ([hermaion.eu](https://hermaion.eu)), so the paperwork happens while you fly.

Everything it does is also on the website. The app adds hotkeys, reading your wallet or a contract off the screen, pausing your run when the game closes, and your position for an SOS.

## Download

Get the latest installer from the hermaion HQ Website, or directly from Github: the file ending in `-setup.exe`. Windows 10 or 11, 64-bit.

It installs for your Windows user only, without admin rights, and updates itself after that.

*The program requires a token from our website to function correctly*

## Install and connect (5 minutes)

1. **Run the installer.** Windows may say it protected your PC, because the installer is not signed with a paid certificate. Choose **More info**, then **Run anyway**.
2. **Make a token on HQ.** Sign in at [hermaion.eu](https://hermaion.eu), open **Profile**, then **Desktop companion**, and choose **Create token**. It is shown once: copy it.
3. **Paste it into the app.** The app opens its Settings window on first start (later: right-click the tray icon, **Settings**). Paste the token and choose **Save and connect**. The tray menu now shows your active contract.

Lost your PC or token? Revoke the token on your HQ profile; the app stops working at once.

## Hotkeys

They work while Star Citizen runs in **borderless windowed** mode. With several screens, the screen-reading hotkeys read the one the game is on. To change one, open Settings, click its box and press the keys you want.

Every hotkey answers: a short tick when it is heard, then a rising sound when it worked or a falling one when it did not, and a small pop-up in the top right corner of the screen. The app uses only its own pop-ups, never Windows notifications: they fade after 7 seconds, have a close button and never take focus from the game. Sounds and pop-ups can each be switched off in Settings.

| Hotkey                | What it does                                                                                                                                                                                                                                     |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Ctrl+Alt+N**        | Moves your active contract to its next stage (Loading, Awaiting clearance, In transit, Unloading, Delivered), exactly as the Dispatch page would.                                                                                                |
| **Ctrl+Alt+W**        | Reads your aUEC balance from the screen and updates it on HQ. Open the mobiGlas home or wallet first.                                                                                                                                            |
| **Ctrl+Alt+F**        | Reads the ship terminal's list (open it in game first) and adds the ships HQ does not have yet to your fleet. Read again after scrolling; nothing is added twice.                                                                                |
| **Ctrl+Alt+R**        | Reads the refinery terminal: the work order you are setting up, or the running one. It goes on your Timers and HQ's Refinery page, and Dispatch messages you when it is done. Reading it twice updates it, never doubles it.                     |
| **Ctrl+Alt+C**        | Reads the contract open in your mobiGlas and sends it to HQ as a draft. Check it on Dispatch and post it with one click.                                                                                                                         |
| **Ctrl+Alt+I**        | Interdicted: logs it on your active run and warns everyone of the spot on HQ's Hazards page and in the planners.                                                                                                                                 |
| **Ctrl+Alt+S, twice** | **SOS**, for critical danger. Press twice within 3 seconds (the first press only gets it ready). Your call goes up on HQ and in #sos-beacon with your ship, your run and your last position from the game's log. Press again later to update it. |

## The cockpit

Click the Hermaion icon by the clock to open the cockpit: everything the app does on one screen.

- **Run**: your active contract with its stages and a countdown to arrival, the next-stage button, and Game crashed, Interdicted and Ask for an escort.
- **SOS**: click Send SOS twice within 3 seconds. While yours is out, it shows who is responding and offers I am safe.
- **Wallet**: your balance on HQ, read it from the screen, and your open payouts.
- **Timers**: your refinery orders and rented ships with the time left. A pop-up says when an order is ready or a rental has 15 minutes left; **Collected** takes an order off the list.
- **Loops**: the best loops in each system for your default ship and money (set both on your HQ profile).
- **Crew**: members with an SOS out, and the last day's price alerts and escorts.
- **HQ**: one click to the pages on the website.
- **Guide**: how everything works, with your own hotkeys, and fixes for common problems.
- **Discord** (bottom of the rail): opens the Hermaion server.
- **Live** in the title bar: connected to HQ's live feed, so an SOS or price alert shows up at once.

Tick **On top** to keep it above the game in borderless windowed mode.

## The tray menu

Right-click the Hermaion icon by the clock:

- Your active contract and its next step, or **Back in game** while it is on hold.
- **Game crashed**, **Interdicted**, **Ask for an escort**, **Send SOS** (or **I am safe** while one is out).
- **Read wallet from screen**, **Read contract from screen**, **Read fleet from screen**, **Read refinery order from screen**.
- Your balance and payouts on HQ.
- **Open in HQ**: SOS, Run planner, Hazards, Escorts, Payouts, Price alerts.
- **Hermaion Discord**: opens the server.
- **Settings**, **Refresh**, and **Install version** when an update is ready.

The app's pop-up confirms every action, and shows price alerts, escorts taken on your runs, members' SOS calls and members answering yours. The cockpit's Crew tab keeps the last day of them.

## When the game closes mid-run

On by default (Settings, "Pause my run when Star Citizen closes"). When Star Citizen closes during a run, a crash or calling it a night, your run goes on hold: the countdown on your contract card stops. When the game is back, the run resumes and its arrival moves back by the time lost.

At that moment the app also reads the end of the game's log and tells HQ where you were and your last quantum exit (mid-jump: where the jump was going). The cockpit's Run tab then offers **Post out for cover**: Escort & Security is pinged in Discord with where to go, and whoever takes it becomes your escort. Managers can post it out for you from HQ's Escorts page.

## Your SOS position

When you send an SOS, the app reads the game's own text log (`Game.log` in the game's `LIVE` folder) and picks out the lines that say where you are: arriving at a station, choosing and finishing a quantum jump, entering a planet's space, going down. HQ turns those into "Area18, ArcCorp" or "Quantum travel from Orbit of Hurston to Orison, Crusader".

Game installed somewhere other than `C:\Program Files\Roberts Space Industries\StarCitizen\LIVE`? Set the path to `Game.log` in Settings.

The game does not document these lines and can change them with a patch, so this is best effort: with nothing found, the SOS goes out with your run instead.

## Safe with Easy Anti-Cheat

The app **never reads the game's memory, never injects anything and never touches the game's process**. It only:

- sees the screen when you press a hotkey, like taking a screenshot;
- sees the game's name in Windows' list of running programs, the way Discord shows which game you play;
- reads the game's own text log when you send an SOS, the way Notepad would;
- reads the keyboard's raw input for your hotkeys, the way game controllers are read: every key goes through to the game untouched, and nothing is kept.

## What is sent, and what is not

- **Sent to HQ:** your balance, a contract's, ship terminal's or refinery terminal's text (HQ keeps only what it finds: the contract, your ships, the order and its time) or a stage change when you press a hotkey; for an SOS, the kind of event, the place code and its time.
- **Never sent:** screenshots (read on your PC and thrown away), your log file (only the few lines that place you, reduced to a code and a time), your PC's name or Windows user name.
- **Your token** is kept in Windows Credential Manager, not in a file.
- **Crash reports** (when the app itself fails) go to the Board's error tracker with tokens, screen text, balances and machine and user names removed.

## Updates

The app looks for a new version when it starts and every hour. When one is ready, a banner across the cockpit says what it brings, with **Install and restart** (or **Later**); the tray menu offers **Install version** too. **Check for updates** in the cockpit's HQ tab or the tray menu asks right away. Every update is signed by Hermaion; the app refuses any update that is not.

## Uninstall

Windows **Settings**, **Apps**, **Installed apps**, **Hermaion Companion**, **Uninstall**. Then revoke its token on your HQ profile.

## Trouble?

| Problem                       | Try                                                                                                                                                                                                 |
| ----------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| A yellow band in the cockpit  | The app is not connected to HQ. It says why; Connect or Settings fixes it, Try again checks at once.                                                                                                |
| "HQ did not accept the token" | Make a new token on your profile and paste it in Settings.                                                                                                                                          |
| "HQ has moved to ..."         | Put the address it names in Settings as the HQ address.                                                                                                                                             |
| A hotkey does nothing         | No tick: the key never reaches the app. Run the game in borderless windowed mode, or pick another combination in Settings (another program may hold it). A tick but no result: the pop-up says why. |
| The wallet is not read        | Open the mobiGlas home or wallet so the aUEC figure is on screen, then press the hotkey.                                                                                                            |
| The SOS has no position       | Check the `Game.log` path in Settings. Right after you spawn, the log may not place you yet.                                                                                                        |
| Windows blocks the installer  | **More info**, then **Run anyway**.                                                                                                                                                                 |

Anything else: ask in the Hermaion Discord.

---

Hermaion Corporation. Secure transport. Complete discretion. Every route, a windfall.

## Code signing policy

Free code signing provided by [SignPath.io](https://about.signpath.io), certificate by [SignPath Foundation](https://signpath.org).

Team roles:
- Committers and reviewers: [the Hermaion HQ maintainers](https://github.com/europalle/hermaion-hq/graphs/contributors)
- Approvers: the repository owner (europalle)

Privacy policy: this program talks to three places. Hermaion HQ, at the address set in its Settings, gets only what the member asks for: their wallet balance, a contract, ship list or refinery order read off the screen, an SOS with their last position from the game log, and status changes on their runs. HQ's live feed (Dispatch) only tells the app when to check HQ again. GitHub is asked for new versions. Screenshots and log files never leave the PC. Crash reports, when switched on by the organisation, go to its error tracker with tokens, screen text, balances and machine and user names removed. Nothing is sent anywhere else.
