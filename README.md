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

The update workflow checks the latest stable GitHub release every six hours. It verifies the release files, SHA-256 checksums and installer signature before committing the new version and checksum. It uses this repository's temporary `GITHUB_TOKEN`; no persistent publishing key is required. Downgrades and changed bytes for an existing version are rejected.

For a manual check, run **Update Corneta** in Actions with `publish=false` (the default). Use `publish=true` from `main` to commit a verified update. Pull requests validate without committing. The verifier is pinned to a reviewed commit of [Corneta](https://github.com/pitroldev/corneta); update that pin when its distribution contract changes.

Corneta source and these manifests are MIT licensed. Bundled dependencies retain their respective licenses. Application support: [pitroldev/corneta](https://github.com/pitroldev/corneta/issues).
