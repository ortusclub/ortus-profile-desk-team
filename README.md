# Ortus Profile Desk downloads

## Install on your Mac

Paste this stable command into Terminal:

```sh
installer=$(mktemp) && curl -fsSL https://raw.githubusercontent.com/ortusclub/ortus-profile-desk-team/main/install.sh -o "$installer" && bash "$installer"
```

It always installs the latest version. No GitHub login, GitHub CLI or Homebrew is required. Alternatively download **Ortus-Profile-Desk-universal.dmg** from [Releases](https://github.com/ortusclub/ortus-profile-desk-team/releases/latest).

Requires macOS 13+ and Google Chrome. Supports Intel and Apple Silicon. Builds are ad-hoc signed, not Apple-notarized. If macOS blocks this trusted download, use System Settings → Privacy & Security → Open Anyway.

## Connect your profiles

Open the app, click **Connect team workspace**, and enter the key supplied by your team administrator. Active accounts and proxies load from the server. The installer is public, but the workspace key and account data are not included. Save and share the key only through your team's private channels.

The app stores the key in its Keychain-encrypted settings. The server refreshes the sheet every five minutes; open apps refresh every ten seconds. New profiles and settings changes appear on connected Macs. Browser login sessions and site storage remain local in this version.

## Updates

Version 0.1.6+ checks and downloads updates automatically without GitHub sign-in. **View update progress** explains Download → Verify → Prepare → Restart. Close profiles and choose **Restart to update** when ready. The Terminal command above also upgrades older versions while preserving saved profiles.

## Developers and releases

Source and development instructions: https://github.com/ortusclub/ortus-profile-desk. Keep this repository name, its main branch and `install.sh` path stable so the installation command does not change.

Every release must include both `Ortus-Profile-Desk-universal.dmg` and `install.json`. Generate these with `node scripts/prepare-release.cjs` in the source repository after building. Neither repositories nor release artifacts may contain production keys or account data.
