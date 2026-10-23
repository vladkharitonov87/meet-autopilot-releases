<div align="center">

# Meet Autopilot

**Your Google Meet calls open themselves — in the right account, with the camera and microphone off.**

[![Latest version](https://img.shields.io/github/v/release/vladkharitonov87/meet-autopilot-releases?label=version)](https://github.com/vladkharitonov87/meet-autopilot-releases/releases/latest)
[![Release date](https://img.shields.io/github/release-date/vladkharitonov87/meet-autopilot-releases?label=released)](https://github.com/vladkharitonov87/meet-autopilot-releases/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/vladkharitonov87/meet-autopilot-releases/total?label=downloads)](https://github.com/vladkharitonov87/meet-autopilot-releases/releases)
![Windows 10 | 11](https://img.shields.io/badge/Windows-10%20%7C%2011-0078D4?logo=windows)

[![Download for Windows](https://img.shields.io/badge/Download_for_Windows-1A73E8?style=for-the-badge&logo=windows&logoColor=white)](https://github.com/vladkharitonov87/meet-autopilot-releases/releases/latest)

<sub>The <code>meet-autopilot-&lt;version&gt;-setup.exe</code> file in the <b>Assets</b> section ·
<a href="https://github.com/vladkharitonov87/meet-autopilot-releases/releases">Release history</a></sub>

</div>

---

> [!NOTE]
> Meet Autopilot is under active development. The first builds in this repository are for testing; the
> list below describes what the app is built to do, not what every build already does.

## What it does

- 📅 **Reads your calendars.** Once a day it reads the events of up to three Google accounts and builds the list of meetings for the day.
- 🚀 **Opens Google Meet by itself.** A few minutes before a meeting starts, the Meet link opens in a new Chrome window without stealing the focus of what you are doing.
- 👤 **Uses the right account.** The meeting opens under the Google account whose calendar it lives in.
- 🔇 **Keeps you muted.** The camera and the microphone are turned off before you join; joining automatically is a setting.
- 🧹 **Skips what you do not need.** Declined and cancelled events, all-day events and events without a Meet link are not opened.
- 🔒 **Keeps your data on your computer.** Settings and sign-in tokens are stored only on this PC (tokens are encrypted with Windows DPAPI); nothing is sent to any server of mine.
- 🔄 **Updates itself.** The tray menu tells you about a new version and installs it.

## Installation

1. Click **Download for Windows** above and download `meet-autopilot-<version>-setup.exe` from the **Assets** section.
2. Run the installer. It installs into your user profile (`%LocalAppData%\Programs\MeetAutopilot`) and does not need administrator rights.
3. The installer is not digitally signed yet, so Windows may warn you:
   - **SmartScreen** ("Windows protected your PC"): click **More info → Run anyway**.
   - **Smart App Control** (on by default on a clean Windows 11) blocks unsigned programs without an "Run anyway" button. If it blocks the installer, the app cannot be installed while Smart App Control is on.
4. Start the app from the Start menu. It lives in the system tray.
5. Click **Sign in with Google** for each account and allow read-only access to the calendar. Google shows a notice that the app is not verified yet — choose **Advanced → Go to Meet Autopilot**.

## Requirements

- Windows 10 or 11 (64-bit); nothing else to install, the app brings its own runtime.
- Google Chrome.

## Verifying a download

Every release has a `meet-autopilot-<version>-setup.exe.sha256` file next to the installer. To check the installer:

```powershell
(Get-FileHash .\meet-autopilot-<version>-setup.exe -Algorithm SHA256).Hash
```

The result must equal the value in the `.sha256` file.

## Uninstall

**Settings → Apps → Installed apps → Meet Autopilot → Uninstall.** Your settings and tokens stay in `%AppData%\MeetAutopilot`; delete that folder to remove them.

## Feedback

Source code is private. Report a problem or an idea in [Issues](https://github.com/vladkharitonov87/meet-autopilot-releases/issues).
