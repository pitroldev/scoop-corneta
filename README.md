# Corneta Scoop bucket

Install [Corneta](https://www.corneta.live/), a free Windows application for local multistreaming, unified chat, and stream replays.

## Install

Requires [Scoop](https://scoop.sh/), Windows 10 or newer (x64), and Microsoft Edge WebView2 Runtime.

```powershell
scoop bucket add corneta https://github.com/pitroldev/scoop-corneta
scoop install corneta/corneta
```

If WebView2 Runtime is missing, install it from Microsoft or use `scoop install extras/webview2` after adding the Extras bucket.

## Update and uninstall

```powershell
scoop update corneta
scoop uninstall corneta
```

Use Scoop for updates. Corneta's in-app updater uses the standalone Windows installer and should not be used for this extracted installation. Settings, accounts, reports, and recordings remain in the Windows profile; uninstalling this package does not delete them.

The manifest downloads the official versioned installer, verifies SHA-256, and extracts the application, FFmpeg, MediaMTX, and third-party notices without running the installer.

## Maintain

Run Scoop's `bin/checkver.ps1 -Dir ./bucket -App corneta -Update` to refresh the version and hash from the upstream release. Review the resulting diff, verify extraction and dependency notices, and commit the update. This repository does not automatically publish new versions.

Corneta source and these manifests are MIT licensed. Bundled dependencies retain their respective licenses. Application support: [pitroldev/corneta](https://github.com/pitroldev/corneta/issues).
