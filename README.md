# Ortus Profile Desk — private team downloads

## Install

Download **Ortus-Profile-Desk-universal.dmg** from [Releases](https://github.com/ortusclub/ortus-profile-desk-team/releases), open it and drag the app into Applications. Requires Google Chrome and macOS 13+; supports Intel and Apple Silicon. This build is ad-hoc signed, not Apple-notarized. If macOS blocks opening your trusted download, use System Settings → Privacy & Security → Open Anyway.

For Terminal installation, install GitHub CLI (`brew install gh` or https://cli.github.com), then run:

```sh
gh auth login --hostname github.com --web --git-protocol https
installer=$(mktemp) && gh api repos/ortusclub/ortus-profile-desk-team/contents/install.sh -H "Accept: application/vnd.github.raw" > "$installer" && bash "$installer"
```

Your GitHub account needs access to this private repository. Since the source repository is now private too, the previous public curl command no longer works.

## Load the shared profiles

In version 0.1.4 or later, choose **Connect team workspace** and enter the workspace key supplied by your administrator. You only need to enter it once on each Mac. Active spreadsheet accounts and their proxy credentials load from the server into folders based on VM Account. New shared profiles and changes appear automatically on other connected Macs.

The key is stored in the Mac's Keychain-encrypted vault. It is not bundled in the app or committed to either repository. Anyone given the key has shared workspace access; give it only to your team.

The server refreshes the account sheet every five minutes and apps refresh every ten seconds. Blank spreadsheet proxy fields use direct connections. Browser login sessions and site storage remain local in this version; they do not transfer between Macs yet.

## Updates

Use **Check for updates** in the sidebar. The app also checks at startup and every four hours, downloads updates in the background, and offers **Restart to update** after all profiles are closed. GitHub CLI must remain signed into an account with this repository's access. Saved profiles and the workspace connection are preserved.

## Developers

Work in **https://github.com/ortusclub/ortus-profile-desk** (private). That repository contains the desktop app, server, tests and deployment manifests. This repository is only for distribution and installation instructions. Ask the owner for collaborator access and the workspace key separately.
