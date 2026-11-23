# Friday

**A voice assistant for Windows that actually runs your computer.**
Say what you want. Friday listens, understands, and does it: opening apps, playing music, answering
questions, reading your messages, finding files, fixing problems, and a great deal more. Most of it works offline.

* Website: [**fridaycore.win**](https://fridaycore.win)
* Download Friday: from [**fridaycore.win**](https://fridaycore.win) or the **Releases** page of this repository (nowhere else)
* Data downloads: [downloads.fridaycore.win](https://downloads.fridaycore.win)
* Author: [l5r431](https://github.com/l5r431)

> Friday is written in Python (PySide6 interface), compiled to a normal Windows program with Nuitka.
> Speech recognition and the voice both run on your own PC.

\---

## Contents

1. [What Friday can do](#what-friday-can-do)
2. [The Friday window](#the-friday-window)
3. [Works offline, respects your privacy](#works-offline-respects-your-privacy)
4. [Install](#install)
5. [Build from source](#build-from-source)
6. [Project layout](#project-layout)
7. [Data, licences and credits](#data-licences-and-credits)
8. [Support Friday](#support-friday)

\---

## What Friday can do

Friday is controlled by voice, by typing in its window, or from your phone through Telegram. You can chain
several commands in one sentence: *"open Chrome and play music and set the volume to fifty percent."*
You don't have to remember exact phrases. Friday also matches what you meant when you say it a different way, and
you can teach it your own words.

### Apps and windows

* Open and close applications, websites and your folders; chain several commands in one sentence.
* Manage windows by name: maximise, minimise, restore, close, snap and tile side by side or stacked, switch between windows, minimise or maximise everything, show the desktop.
* Kill running processes, list what is open, reopen a frozen app.
* Install, uninstall and update applications (always asking you first); snapshot and restore your installed apps.
* Custom **modes** (gaming, developer, anything you define) that open a whole set of apps at once.

### Music and media

* Play music by song, artist or kind, control playback and volume, say what is playing, download the current song, switch the audio output device.
* **Tempo sessions:** say *slow music*, *fast music* or *normal music* (also *soft*, *calm*, *chill*, *upbeat*, *party*, *workout*, *medium* and many more). Friday keeps to that kind of music until you stop it or ask for something else.
* Queues and playlists by voice: create them, add the current song, play and shuffle.
* Controls for short-video sites, and a built-in video library and player.
* Music ducks politely when Friday speaks.

### Typing, dictation and conversation

* **Dictation mode** types what you say into any app.
* **Assistant mode** holds an ongoing conversation.
* A **chat tab** where you pick the mode (chat or image creation) and which AI model answers.
* **Image creation** from a text description, saved to *Pictures → Friday Pictures* (follows OneDrive).
* Speaks answers with a natural offline voice (Piper); convert any text to speech and download it.

### Questions and answers

* A layered answer chain: online AI with search where available, then DuckDuckGo, then a local model (Ollama) when offline.
* Bring your own keys for Claude, ChatGPT, Gemini, Groq, Cloudflare, OpenRouter or a custom endpoint; all optional.
* Weather, local and international news, the time anywhere in the world, quick maths, unit conversions and date maths.
* Reads a web page, PDF, text file or document aloud.
* **Screen help:** *"what is on my screen?"* or *"what is wrong with this?"* explains an error or helps with whatever you are working on.

### Maps, places and routes

* Nearest hospitals, schools, pharmacies and more: spoken names, distances and drive times, with the route opened in Google Maps when you are online.
* A world map window with towns, villages and roads that appear as you zoom, and country facts and history when you click a country (Friday can read the history aloud).
* **Offline** place names (GeoNames) and offline road routing from downloadable per-country road packs, with travel-time estimates.
* Download place data, road data and world history from the settings page or by voice (*"download road data for Kenya"*).

### Time, timers and reminders

* Timers and reminders by voice (*"thirty minutes"* starts a timer), with an alarm sound.
* A simple **Timers \& Focus** page: set a timer, a reminder or a Google Calendar event with plain boxes, no wording to remember.
* Timed **focus sessions** and Do Not Disturb control.
* Google Calendar: read your day, create events by answering *what, which day, what time*, and be reminded before events start.
* Hourly time announcements, health reminders and low-battery warnings.

### Messages and email

* Unread email from several Gmail accounts, Discord messages, Telegram and WhatsApp messages, and Windows notifications.
* Send Telegram and WhatsApp messages by voice.
* **Telegram bridge:** send Friday commands from your phone and get the replies there.
* A **catch-up** after the internet comes back, and a morning briefing (weather, news, calendar, message counts, system health, recommendations).
* Daily, weekly and monthly reports on your computer and app usage.

### Files

* Instant file search (powered by Everything) and a file-search window on **Alt+Space**.
* Find a file by name and Friday remembers it, so you can then say *compress it, extract it, convert it, rename it, copy it, move it to a folder, show it, delete it*, even when File Explorer is closed.
* Convert files and documents (including PDFs), compress and extract archives, from the interface or the right-click menu in File Explorer.
* Download videos, music and shareable links by pasting a link.
* Organise your desktop and folders, find duplicate and large files, clean up the disk, empty the recycle bin; destructive actions have undo where possible.

### Control the computer without a mouse

* Move the mouse, scroll, click, right-click and double-click by voice.
* **Show numbers:** numbers appear on everything clickable; say a number to click it. Works on a chosen app or the taskbar, with a keyboard shortcut for toggling.
* **Show grid** when an app has nothing clickable: narrow it down box by box.
* Select several files by number (*"select one to five"*) and copy, cut, delete, compress or rename them.
* Screenshots, screen recording, lock, shut down, restart, mute the microphone (Ctrl+Alt+M).
* Switch wallpaper and light/dark theme.

### Fix problems

* Network diagnostics with a narrated retry loop, DNS flush, audio, Bluetooth and printer restart, frozen Explorer fix.
* Full system status (CPU, GPU, RAM, disk) with recommendations.
* Friday's own crash reporter and stall watchdog.

### Memory and learning

* Remembers personal facts when you ask and recalls them later; tells you how much it remembers; clears it on request.
* Learns your routines and makes suggestions; learns new phrasings and words you teach it.

\---

## The Friday window

|Tab|What it is for|
|-|-|
|**Overview**|Status, quick actions, ABOUT, **CREDITS** and **DONATE** buttons|
|**Chat**|Talk to Friday in text; choose chat or image creation and the AI model|
|**Commands**|Every command and its trigger phrases; edit or add your own|
|**Conversation**|The running log of what you said and what Friday answered|
|**Timers \& Focus**|Set timers, reminders and calendar events; see the active ones|
|**Files, Converter, Downloader, Wallpaper, Songs, Streaming, TTS, Modes, Restore, App Updates**|The tools described above, each with its own page|
|**Settings**|Everything configurable, including accounts, offline data downloads and keys|

\---

## Works offline, respects your privacy

* Speech recognition (Moonshine) and the voice (Piper) run **on your PC**. Friday does not send your voice to a server.
* A local AI model (Ollama, gemma3:1b) answers questions when there is no internet.
* Place names, the world map, country histories and road routing work offline once their data is installed.
* Calendar events are cached so Friday can read them offline.
* Secrets such as API keys and tokens are stored encrypted for your Windows account (DPAPI).
* Online features (news, weather, AI search, messages, maps lookups) are used only when you ask for them and are clearly the exception, not the rule.

\---

## Install

**Requirements:** Windows 10 or 11 (64-bit), a microphone, about 2 GB of free disk space, and an internet connection for the first-time data download.

**Where to get Friday.** Friday is distributed in only two places, both run by its author:

* the download on [**fridaycore.win**](https://fridaycore.win), and
* the **Releases** page of this repository (the installer is attached to each release).

Please do not use copies from other websites, file-sharing sites or third-party app stores: they are not from the author and can be
changed or contain malware. Every release page lists the installer's SHA-256 so you can check what you downloaded.

1. Download **Friday-Setup-x.y.z.exe** from one of the two places above.
2. Run it. No administrator rights are needed for the app itself (it installs for your user).
3. On first install, Friday downloads its models and voices (about 1.3 GB, once) from `downloads.fridaycore.win`. An **offline installer** that includes them is also available from the same two places.
4. The installer can also set up Ollama and the offline AI model, and the Everything file-search service (Windows asks for permission once for that).
5. Friday updates itself quietly from the same two sources and only re-downloads big data when it changes.

More information, news and help: [**fridaycore.win**](https://fridaycore.win).

\---

## Data, licences and credits

Friday stands on the work of many open projects and data sets. The full, searchable list (who made each tool, what Friday uses
it for, and its licence) is in the app: **Overview → CREDITS**, and in `core/credits.py`. Highlights:

* **OpenStreetMap** (© OpenStreetMap contributors, ODbL): maps, places, road packs. **GeoNames** (CC BY 4.0): place names.
* **CIA World Factbook** (public domain): country facts and history.
* **Piper**, **Moonshine**, **Ollama**, **Everything**, **mpv**, **FFmpeg**, **yt-dlp**, **Qt / PySide6**, **Nuitka** and many Python libraries.
* Weather by Open-Meteo; movie data by TMDB where used.

If you ship or fork Friday, keep the attribution these licences require, and review each dependency's terms for your use.

**Licence:** Friday's source is currently *all rights reserved*. A licence will be added if the project is opened up.

\---

## Support Friday

Friday is free. If it helps you and you would like to support its development, donations are welcome and unlock nothing.
Use the **DONATE** button on the Overview page, or say *"support Friday"*.

USDT on the **Tron (TRC-20)** network only:

```text
TPrqsPjruu4nbcCQxjgMeHX7Pvtkn9VbTG
```

Sending any other coin or network to this address can lose the money. Thank you!

\---

© 2026 l5r431 · [fridaycore.win](https://fridaycore.win)

