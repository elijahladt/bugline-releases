# Scoreline — releases

Built installers for **Scoreline**, a desktop live-sports ticker widget.

This repository contains **no source code**. It exists only to host release
binaries so the app can auto-update itself: the source lives in a private
repository, and `electron-updater` needs a publicly readable location to
fetch `latest.yml` and the installer from.

## Install

Download the latest `Scoreline-Setup-*.exe` from
[Releases](../../releases/latest) and run it.

Once installed, the app checks for updates on launch and installs them on the
next restart — you only need to download manually the first time on a machine.
