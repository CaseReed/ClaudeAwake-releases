# ClaudeAwake

Keep your Mac awake with the lid closed, without letting it overheat.

ClaudeAwake is a small menu bar app for MacBooks with Apple silicon. Close the lid and your Mac keeps
running: long downloads, builds and other tasks carry on. Meanwhile ClaudeAwake watches the CPU temperature
and the battery, and lets your Mac go to sleep normally if it gets too hot or the battery runs low.

**[Download the beta](https://github.com/CaseReed/ClaudeAwake-releases/releases)** · macOS 26 or later ·
Apple silicon · free during the beta

## Install

1. Download the DMG from the [latest release](https://github.com/CaseReed/ClaudeAwake-releases/releases),
   open it and drag ClaudeAwake to Applications.
2. Open ClaudeAwake. The beta is not notarized by Apple yet, so macOS says it cannot verify it: click Done.
   Then open System Settings › Privacy & Security, click Open Anyway next to ClaudeAwake, and confirm.
3. The welcome window does the rest: install the system helper, then allow it in
   System Settings › General › Login Items & Extensions.

## What it does

- **Lid closed mode.** Turn it on from the menu bar icon or with ⌥⌘A. Keep it on until you turn it off,
  or for 1, 2 or 4 hours.
- **Safety sleep.** ClaudeAwake notifies you as the CPU warms up (85 °C by default). At your sleep threshold
  (90 °C by default, 75 to 100 °C) it lets your Mac go to sleep. Your session is right where you left it.
- **Battery floor.** On battery, it lets your Mac sleep when the charge falls to 15 % (10 to 25 %, or off).
- **At a glance.** The temperature in the menu bar if you want it, and the display turns off when you close
  the lid.

## How it stays safe

Keeping a Mac awake with the lid closed needs a small system helper, which you approve once in
System Settings. It does one thing: it disables sleep while the app keeps renewing a short lease of about
90 seconds.

- If ClaudeAwake quits, crashes or freezes, the lease runs out and your Mac gets its normal sleep back.
- Turning the mode off, or a safety sleep, gives it back right away.

## Privacy

There is no account and no analytics. The only network request is the daily update check, which reads
`appcast.xml` from this repository. Logs stay on your Mac until you export them and send them yourself.

## Updates and the end of the beta

ClaudeAwake checks for a new version once a day and asks before installing it. You can also check from
Settings › General › Check for updates. Each beta works until the date shown there. After that, lid-closed
mode stays off until you install a newer version.

## Feedback

Tell the person who shared the beta with you what happened, when, and what you expected. To help, export
the logs from Settings › General › Diagnostics › Export… and attach the zip. It holds the app's temperature
and battery samples, its events, your settings and your Mac's model.

## Uninstall

Quit ClaudeAwake from its menu and move it to the Trash. If it still shows in
System Settings › General › Login Items & Extensions, switch it off there.

---

ClaudeAwake is free during the beta and provided as is, without warranty. All rights reserved.
