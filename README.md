# BoostPing

**A free tool that tunes Windows network settings for gaming with a single button, making online games more responsive.**

English · [한국어](README.ko.md) · [简体中文](README.zh-CN.md) · [日本語](README.ja.md) · [Español](README.es.md) · [Português (Brasil)](README.pt-BR.md) · [Français](README.fr.md)

> This document is a translation. If anything differs, the [Korean version](README.ko.md) is authoritative.

![Platform](https://img.shields.io/badge/platform-Windows%2010%20%2F%2011%20(64--bit)-0078D4)
![License](https://img.shields.io/badge/license-Freeware-brightgreen)
[![Download](https://img.shields.io/badge/download-kilho.net-orange)](https://down.kilho.net/boostping?lang=en)

![BoostPing screen](images/boostping-en.png)

## Overview

By default, Windows collects network data for a moment and sends it in batches. That is efficient for downloads and web browsing, but in online games — where every keystroke needs to reach the server right away — it makes the game respond later.

BoostPing changes five of these settings to suit games. Press **Start Boost** and it finds the network you are connected to the internet with, applies the settings, and reconnects the network. Press **Turn Off Boost** and it puts back exactly the values you had before. You choose which items to change, and items you leave unchecked are never touched.

## Features

- **One button** — No complicated setup; a single press of Start Boost is all it takes.
- **Finds your active network automatically** — Picks the adapter actually connected to the internet and shows its name and IP at the bottom of the window. Virtual network adapters are skipped.
- **Five items, applied as you choose** — Instant ACK, No ACK Delay, Disable Nagle's Algorithm, Remove Network Throttling, Prioritize Games.
- **Exact restore** — Remembers the values from before the boost and puts them back when you turn it off. Settings that didn't exist are removed, and values you had changed yourself return to those values.
- **Stays on after you close it** — The settings are applied to Windows, so the effect continues after you close the window or reboot. Run it again and it shows the applied state as it is.
- **9 languages** — Korean · English · Japanese · Chinese · Russian · Italian · French · Arabic · Spanish. Follows the Windows display language.

## Download / Installation

| Type | Link |
|---|---|
| Installer | [Download](https://down.kilho.net/boostping?lang=en) |
| Portable (ZIP) | [Download](https://down.kilho.net/boostping?lang=en&nosetup) |

The installer starts BoostPing right after installation finishes. For the portable version, unzip it and run `BoostPing.exe`. Either way, it asks for **administrator rights**.

## Usage

### Getting started

1. Run BoostPing. Because it changes Windows settings, an administrator permission prompt appears — click **Yes**.
2. Check that the name and IP of the network you are using appear on the bottom line. (e.g. `Ethernet (Realtek PCIe GbE Family Controller) · 192.168.0.10`)
3. To choose which items to change, click the **settings icon** at the top right to open the **TUNING** screen. All five items are on at first.
4. Click **Start Boost**. The status changes to **BOOST** and "Reconnecting the network…" is shown. The internet drops briefly and reconnects at this point.
5. Once the internet is back, the status changes to **ON** with "Optimization is applied". Now start your game.
6. To return to how things were, click **Turn Off Boost**. The network reconnects once more and the status goes back to **READY**.

### Screen layout

**Main screen**

| Element | Description |
|---|---|
| **BOOST//PING** logo | Opens the BoostPing homepage |
| Settings icon (top right) | Opens the TUNING screen |
| **STATUS** | **READY** = standby, **BOOST** = applying, **ON** = applied |
| 5 bars · **%d / 5 items** | Number of items turned on; one bar per item |
| **Start Boost** / **Turn Off Boost** | Apply / restore the original settings |
| Bottom line | Name · IP of the network in use, program version |

**TUNING screen** — Click an item to turn it on or off. Changes are saved immediately.

| Item | What it does |
|---|---|
| **Instant ACK** | Sends acknowledgements right away instead of batching them |
| **No ACK Delay** | Sets the delayed-ACK timer to 0 |
| **Disable Nagle's Algorithm** | Sends small packets immediately without bundling |
| **Remove Network Throttling** | Lifts the transfer limit applied during media playback |
| **Prioritize Games** | Stops reserving CPU time for background tasks |

### Tips for common situations

**When your inputs feel a beat late in a game**
Click Start Boost in BoostPing before launching the game. Online games that exchange small bits of data frequently are where you'll notice it most. Since the internet reconnects briefly when the boost is applied, turn it on **before** you join a match.

**When you want to turn it on once and keep it**
After turning the boost on, you can close the BoostPing window. The settings stay in Windows, so they remain applied even after a reboot. When you run BoostPing again, the status shows **ON**.

**When you play with music or a stream running**
Windows limits network transfers while media is playing. With **Remove Network Throttling** on, that limit doesn't kick in even with music or video playing.

**When you only want some of the items**
While the boost is off (READY), go to the settings icon → TUNING screen and click the items you don't want to turn them off. The bars and **%d / 5 items** on the main screen update right away. Items you turned off are never touched, either when starting or when turning off.

**When you want to change items while the boost is on**
While the boost is on, the TUNING screen is locked and shows "You can change these after turning off the boost." Do it in this order: Turn Off Boost → change items → Start Boost.

**When you want to compare the difference**
Play one round in the original state with Turn Off Boost, and one with Start Boost. Turning it off restores exactly the values from before, so you can switch back and forth as many times as you like.

**When you had changed network settings yourself before**
BoostPing remembers the current values before it starts. When you turn it off, it returns to **the values you had set**, not to the Windows defaults.

**When you switch between Wi‑Fi and wired on a laptop**
The boost applies to the network that was in use when you started it. If you've switched networks, click Turn Off Boost, then close BoostPing and run it again. When the new network appears on the bottom line, click Start Boost. Turning it off always restores the network it was first applied to, even if you've switched since.

**When you're done playing and want things back to normal**
Run BoostPing and click Turn Off Boost. Turn the boost off first before uninstalling the program, too.

**When you can't see the BoostPing window**
Only one BoostPing runs at a time. Running it again while it's already open brings the existing window to the front (and restores it if it was minimized).

## Configuration

Changed on the TUNING screen and saved immediately. Settings are kept across updates.

| Item | Default |
|---|---|
| Instant ACK | On |
| No ACK Delay | On |
| Disable Nagle's Algorithm | On |
| Remove Network Throttling | On |
| Prioritize Games | On |

The interface language follows the Windows display language (Korean · English · Japanese · Chinese · Russian · Italian · French · Arabic · Spanish; English otherwise). Arabic is displayed right to left.

## Requirements

- Windows 10 · Windows 11 (64-bit)
- Administrator rights — because it changes Windows network settings, a permission prompt appears at launch.
- No additional runtime required.

## Updates

BoostPing does **not** update itself. At launch it checks whether a new version exists and shows a notice; pressing **Yes** opens the download page and quits the program. New versions are released manually after internal verification and announced on the [BoostPing page](https://kilho.net/boostping). See the [update policy notice](https://en.kilho.net/archives/notice/2940).

## License

BoostPing is **freeware**. You can use it for free anywhere — at work, at home, in government offices or at school — and redistribute it freely.

## Links

- Website: <https://kilho.net/boostping>
- Forum: <https://kilho.top/forum/qna>
- X (Twitter): <https://www.twitter.com/kilhonet>

© KILHO.NET
