# Blunote Updates

Official Windows installers and update manifests for Blunote.

- Downloads: [GitHub Releases](https://github.com/blunote-app/updates/releases).
- Current Windows updater manifest: `latest-win-v2.json`.
- Immutable version records: `releases/<version>/`.
- Desktop source: private `blunote-app/desktop` repository.
- Website and cloud API source: private `blunote-app/web` repository.

Existing v0.1.52 installations still read `xiaomaolu/blunote-updates/main/latest-win-v2.json`. That compatibility entry is retained and points to the same installer and SHA256 as this repository. Do not delete or rename it while those clients are supported.

Publish release assets and verify them before advancing either manifest. Never overwrite an installer for an already published version. Roll back the latest manifest via a new Git commit if necessary; this stops further offers but does not downgrade clients that already installed a newer version.

Windows v0.1.53 follows v0.1.52's unsigned distribution. Its updater verifies SHA256 and size. Note synchronization covers document, quick-note and whiteboard title/content/archive/pin state; it does not synchronize complete spaces, standalone attachments, folders, tags, comments or custom attributes.
