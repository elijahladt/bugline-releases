# Bugline — releases

Current version: **1.6.11**

Built installers for **Bugline**, a live sports score bug for your desktop —
a broadcast-style ticker along the bottom of the screen, or a corner box,
covering NFL, CFB, NBA, NHL, MLB, EPL and UCL.

**[Download page](https://elijahladt.github.io/bugline-releases/)** ·
**[Run it in a browser](https://bugline-live.vercel.app)** ·
**[All releases](../../releases)**

This repository contains **no source code**. It exists to host release binaries
so the app can auto-update itself: the source lives in a private repository, and
`electron-updater` needs a publicly readable location to fetch `latest.yml` and
the installer from. The download page is served from this repo with GitHub Pages.

## Install

| Platform | File | |
| --- | --- | --- |
| Windows | `Bugline-Setup-1.6.11.exe` | tested |
| macOS · Apple Silicon | `Bugline-1.6.11-arm64.dmg` | untested |
| macOS · Intel | `Bugline-1.6.11.dmg` | untested |
| Linux · x86_64 | `Bugline-1.6.11.AppImage` | untested |

Grab one from [the latest release](../../releases/latest) and run it.

Windows and Linux check for updates on launch and install them on the next
restart, so you only download manually the first time on a machine.

### macOS needs one extra step

The builds are unsigned, so the first launch is refused with "Bugline is
damaged and can't be opened." It isn't damaged — that is what macOS says about
anything it cannot verify. Drag it to Applications, then:

```sh
xattr -dr com.apple.quarantine /Applications/Bugline.app
```

Auto-update does not work on unsigned Mac builds, so a new version means a new
download.

### Linux needs X11

Wayland will not let an application place itself above other windows, which is
the whole job here — pick "on Xorg" at the login screen. Make the AppImage
executable first; on Ubuntu 22.04 and later it may need
`--appimage-extract-and-run`.

## No install

Bugline also runs as a web page at **[bugline-live.vercel.app](https://bugline-live.vercel.app)**,
which is the only option on a Chromebook: an app in the Linux container cannot
float above ChromeOS windows. Press **Pop out** and it lifts into a small window
that stays on top of everything else. On a phone there is no pop-out — mobile
browsers do not offer one — so it fills the screen as the box instead.
