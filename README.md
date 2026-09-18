# Ortus Profile Desk — private team downloads

## Install on your Mac

Your GitHub account must have access to this private repository. Open Terminal and paste:

```sh
installer=$(mktemp) && curl -fsSL https://raw.githubusercontent.com/ortusclub/ortus-profile-desk/main/scripts/install.sh -o "$installer" && bash "$installer"
```

The installer downloads the latest private release, verifies it and installs it in Applications. It installs GitHub CLI via Homebrew if needed and prompts for GitHub sign-in. Without Homebrew, install GitHub CLI from https://cli.github.com first and rerun the command. Install Google Chrome to open profiles. macOS 13 or later is required; Intel and Apple Silicon are supported.

Alternatively, download **Ortus-Profile-Desk-universal.dmg** from [Releases](https://github.com/ortusclub/ortus-profile-desk-team/releases), open it and drag the app into Applications. If macOS blocks the app, use System Settings → Privacy & Security → Open Anyway for this trusted team download. The current app is ad-hoc signed, not Apple-notarized.

## Updates

The sidebar shows the current version and **Check for updates**. The app checks automatically at startup and every four hours, downloads newer releases in the background, then offers **Restart to update**. Close profile windows before restarting. GitHub CLI must remain installed and signed into an account with access to this repository. Existing saved profiles are preserved.

## Current status

**0.1.3 is an installer/update preview with local profiles. Shared profiles and saved browser-session synchronization are not enabled yet.** A later private build will connect to the shared workspace automatically.

Source: https://github.com/ortusclub/ortus-profile-desk. Never commit workspace credentials, browser sessions or account passwords to either repository.
