# Ortus Profile Desk — private team distribution

This private repository is reserved for team-only Mac installers of Ortus Profile Desk. Generic application source remains at https://github.com/ortusclub/ortus-profile-desk.

## Planned team build

- Preconfigured connection to a single shared Ortus workspace.
- No individual login or manual workspace-code entry initially.
- Shared profiles seeded from active account-sheet rows and grouped by VM Account.
- New profiles and saved changes synchronize between connected installations.
- Exclusive profile access prevents conflicting browser-session writes.

No shared service or team installer has been deployed yet. The hosting target and live-session behavior are still being confirmed.

Team connection credentials must only be included in private build artifacts. They must never be added to the public source repository or public releases. Live browser-profile data belongs in the shared service, not this code repository.

Access to the eventual team installer grants workspace access. Distribute it only to authorized team members. Repository access is limited to invited collaborators.
