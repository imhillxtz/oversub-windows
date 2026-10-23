<div align="center">

<img src="Docs/images/icon.png" width="128" alt="OverSub icon">

# OverSub for Windows

Vietnamese subtitles and voice for games on your Windows PC, with a controller, touch, keyboard or mouse.

OverSub reads the text in a game on screen, translates it with AI, shows the translation on top of the original text and reads the dialogue aloud in a Vietnamese voice. It works with Windows games running on the PC and with consoles (Switch, PlayStation, Xbox) through a capture card.

[![Download the latest version](https://img.shields.io/github/v/release/imhillxtz/oversub-windows?include_prereleases&label=Download&color=F96B3F)](https://github.com/imhillxtz/oversub-windows/releases)
![Windows 11 x64](https://img.shields.io/badge/Windows%2011-x64-555)
![All rights reserved](https://img.shields.io/badge/license-all%20rights%20reserved-555)

[Tiếng Việt](README.md) · English

</div>

This repository holds only the installer and the documentation. The source code of OverSub for Windows is not published. The Mac version is at [imhillxtz/oversub-mac](https://github.com/imhillxtz/oversub-mac).

OverSub for Windows is in testing: releases are marked Pre-release and may still have bugs.

## What OverSub does

- Subtitles: reads the dialogue in the region you select, translates it and shows the translation over the game's subtitle box. You can also use Floating subtitles, a separate subtitle strip above the game that you can drag anywhere.
- Voice: reads the translated dialogue aloud with the VieNeu Vietnamese voice, which runs on the PC. Dialogue is read before other on-screen text; the next line is prepared while the current one is playing, and when lines come quickly the voice speeds up a little to keep pace.
- Screen translation: translates text outside the dialogue, such as menus, quest logs and item descriptions.
- Dialogue history: look back at translated lines and replay them. Fixed text on screen (logos, labels) can be ignored so it is never translated or read again.
- Each game remembers its own regions, genre and language. The genre (medieval, wuxia, anime and others) guides the AI's choice of Vietnamese forms of address and tone. OverSub remembers how each character has addressed others and uses that for their later lines.
- Fully usable with a controller, touch, keyboard only, or keyboard and mouse (see How it differs from the Mac version).
- Interface in Vietnamese and English. Translates into 12 languages; languages other than Vietnamese use the voices built into Windows.

## How it differs from the Mac version

The Mac version is made for Macs with a mouse and keyboard. Windows PCs come in more shapes: desktops, laptops, 2-in-1s and tablets with touch screens, handheld gaming PCs. The Windows version is designed so that every OverSub screen works with a controller, touch, keyboard or mouse, and you can combine them to suit your device and the moment: touch and shortcuts on a 2-in-1, a controller and touch on a handheld, keyboard and mouse on a desktop. OverSub switches its button hints to whatever you used last, and the play mode screen shows the name of your device.

| Input | In OverSub |
|---|---|
| Controller | Every screen works with the D-pad, A and B; LB and RB switch tabs in Settings. In a game, hold View and press another button. |
| Touch | Touch targets are at least 48 points tall. Drag the region box with your finger, double-tap to enlarge the picture, tap the screen to show the buttons. The on-screen keyboard appears when you need to type a key or a game name and goes away when you're done. |
| Keyboard only | Tab, the arrow keys and Enter move through the buttons; Ctrl Tab switches tabs in Settings. In a game, use the Ctrl Alt shortcuts. |
| Keyboard and mouse | Moving the mouse or typing hides the controller hints and switches the in-game list to Ctrl Alt; pressing a controller button switches back. |

### Xbox Full Screen Experience

If your PC uses the Xbox Full Screen Experience, Windows sends controller input only to the app in front, which is the game. OverSub reads the controller through Windows GameInput, so holding View still reaches OverSub while you play. The Xbox app, Armoury Crate, Steam, Playnite and other launchers are never read; OverSub reads only while a game is in front. If Steam Input turns the controller into keys (the desktop layout), OverSub maps those keys back to controller buttons on its own screens.

## Three ways to play

Each time it opens, OverSub asks "What are you playing today?" with the option you used last time already selected. You can switch at any time with Change how you play.

### Play games on this PC

Windows games opened from Steam, Epic, Xbox or the device's launcher. Press Start, then open a game; the translation appears over the game's subtitle box and a Vietnamese voice reads it. OverSub reads only while a game is in front, not the Windows desktop or game launchers. In the game, hold View and press a button to select regions, pause or bring OverSub back (see In-game controls).

### Watch and play through a capture card

The console's picture and sound play on this PC, with the translation over the picture. You can watch full screen; double-tapping the picture also goes full screen.

### Play on the TV

The console outputs to the TV through a capture card, and the Windows PC sits next to the TV as a reading screen: large dialogue lines, the voice, and translated menus with the picture. The reading screen has the dialogue history and a Replay button, and works with touch or a controller.

## Requirements

- Windows 11 on an x64 PC: a desktop, laptop, 2-in-1 or handheld. Windows 10 version 2004 or later can install it, but it hasn't been tested there.
- A Gemini or Groq API key for translation. Both have free tiers; see Adding translation keys.
- Python 3.13 or 3.12 and the `vieneu` package for the Vietnamese voice. The installer doesn't include them; see Vietnamese voice. Without them OverSub still translates and shows text, it just doesn't read aloud.
- The two capture card modes need a webcam-class (UVC) capture card with a 1080p MJPEG stream. OverSub has been tested with a Hagibis capture card.
- The Windows text recognition pack for the game's language. English is usually installed already; for other languages the app tells you to add it under Settings → Time & language → Language & region. On Windows 11, if Snipping Tool is installed, OverSub uses its text reader (OneOCR), which handles small text better.

The installer includes .NET, so you don't need to install .NET separately.

## Installing

1. Go to [Releases](https://github.com/imhillxtz/oversub-windows/releases) and download `OverSub-Setup-x.y.z.exe` from Assets.
2. Open the downloaded file. The installer isn't digitally signed yet, so Windows SmartScreen shows "Windows protected your PC". Click More info, check that the file name is `OverSub-Setup-x.y.z.exe`, then click Run anyway. Your browser may also say the file isn't commonly downloaded; choose Keep.
3. Follow the installer. OverSub installs for your Windows account into `%LOCALAPPDATA%\Programs\OverSub`, needs no administrator rights, and adds a Start menu shortcut.

You can check that the download is the official build with the SHA-256 file attached to each release. In PowerShell:

```powershell
Get-FileHash .\OverSub-Setup-x.y.z.exe -Algorithm SHA256
```

Compare the result with the contents of `OverSub-Setup-x.y.z.exe.sha256` on the Releases page.

OverSub doesn't update itself yet. To be notified about new versions, click Watch → Custom → Releases at the top of this repository. To update, run the new version's installer; your settings and keys are kept.

## Adding translation keys

1. Get a free key from [Google AI Studio](https://aistudio.google.com/apikey) (Gemini) or [Groq](https://console.groq.com/keys).
2. Open OverSub, click Settings and choose the Translation tab.
3. Paste the key into Gemini keys or Groq keys and click Add. The app tests the key first and adds it only if it works.
4. Click Save.

| Service | Notes |
|---|---|
| Gemini | The best translations among the free options. Limits apply per Google Cloud project, so several keys from one project share the same limit. |
| Groq | Very fast. When Gemini fails or takes longer than 2.5 seconds, Groq translates that line instead. |

Adding both gives you a fallback. If the AI translation hasn't arrived after 1.5 seconds, the app shows a temporary Google Translate version (no key needed) and replaces it when the AI version comes in; turn this off with Show a Google Translate version while waiting for AI on the Translation tab. Free limits are set by each provider and can change.

## Vietnamese voice

The Vietnamese voice uses [VieNeu-TTS](https://github.com/pnnbao97/VieNeu-TTS) (Apache 2.0 license), which runs on the PC through Python. Set it up once as follows; you need an internet connection:

1. Open Terminal (right-click Start → Terminal) and install Python 3.13:

   ```powershell
   winget install -e --id Python.Python.3.13 --scope user
   ```

   If you download it from [python.org](https://www.python.org/downloads/windows/) yourself, pick the "Windows installer (64-bit)" of Python 3.13 or 3.12 and install it with the default options. Python from the Microsoft Store doesn't work.

2. Install the voice package:

   ```powershell
   & "$env:LOCALAPPDATA\Programs\Python\Python313\python.exe" -m pip install vieneu
   ```

3. Open OverSub again. The first time, VieNeu downloads its voice model from Hugging Face, so it takes longer; after that the voice is ready within a few seconds.

The Voice tab in Settings has two voice models, Nano (fast, the default) and Turbo (better, slower), with a Preview button. If the voice doesn't start, the line under Voice explains why, and the log on the General tab has the details.

## In-game controls

When you play on the PC, buttons also reach the game, so OverSub uses View plus another button. Without a controller, use the Ctrl Alt shortcuts. Hold View a little longer in the game and this list appears in the top left corner.

| Action | Controller (hold View, then press) | Keyboard |
|---|---|---|
| Select the subtitle and screen regions | X | Ctrl Alt R |
| Replay the last line | Y | Ctrl Alt Space |
| Pause or resume | B | Ctrl Alt P |
| Hide or show the translation | A | Ctrl Alt H |
| Turn screen translation on or off | RB | Ctrl Alt T |
| Turn the floating subtitles on or off | LT | Ctrl Alt J |
| Move and resize the floating subtitles | RT | |
| Ignore the current line from now on | LB | |
| Open the OverSub window | Menu | Ctrl Alt O |

## Privacy and data

Screen images and capture card video never leave the PC; text recognition runs on the PC. The VieNeu voice runs on the PC as well.

Only text is sent out for translation. The services you added keys for receive the line to translate, a few earlier lines as context, and character names. Google Translate receives text for the temporary versions of dialogue and screen translation. If you don't want text sent to Google Translate, go to the Translation tab, turn off Show a Google Translate version while waiting for AI, and set Screen translation speed to Wait for AI.

OverSub has no server of its own, collects no statistics and shows no ads. Keys are stored in `%LOCALAPPDATA%\OverSub\keys.bin`, encrypted by Windows for your user account. Settings, game profiles and translation memory are also in `%LOCALAPPDATA%\OverSub`. Diagnostic logs are in `%LOCALAPPDATA%\OverSub\Logs` and contain the text read from your games.

## Uninstalling

Go to Settings → Apps → Installed apps, find OverSub and click Uninstall. The `%LOCALAPPDATA%\OverSub` folder (settings, keys, logs) is kept so a later install can pick it up; delete that folder to remove everything. Python and the `vieneu` package are uninstalled separately.

## Current limitations

- The installer isn't digitally signed, so SmartScreen warns the first time you open it.
- There's no build for Windows on ARM yet.
- No automatic updates yet.
- The Vietnamese voice needs Python installed separately. During the first 7 seconds or so after the app opens, while the voice is loading, dialogue may appear as text without being read.
- This version has been tested thoroughly on one device (a ROG Ally) with one type of capture card. If OverSub doesn't work right on your PC, please report it in an Issue.

## Bug reports and feedback

Please open an [Issue](https://github.com/imhillxtz/oversub-windows/issues) with your OverSub version, your device, the game and how you play (on the PC, watch and play, or on the TV). If you can, attach the latest log file from `%LOCALAPPDATA%\OverSub\Logs` (Settings → General has an Open folder button). Please read the log before sending it, since it contains text from your game.

## Support

OverSub is free for everyone. If you find it useful, you can buy me a coffee at [paypal.me/ngochieuit](https://paypal.me/ngochieuit). Starring this repository or recommending OverSub to a friend is another way to help.

## License

© 2026 imhillxtz. All rights reserved.

OverSub is free to use but it is not open-source software, and the source code of the Windows version is not published. Redistributing the installer, modifying the program or reverse engineering it requires written permission from the author. See [LICENSE](LICENSE) for details.

The installer includes the .NET runtime and a few open-source libraries under their own licenses, listed in `THIRD-PARTY-NOTICES.txt` in the installation folder. Game titles and trademarks mentioned here belong to their respective owners. OverSub uses services from Google and Groq under each provider's terms.
