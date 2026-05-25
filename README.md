# beam-ota-updates

Manifest pointers for Beam Live OTA JS-bundle updates.

## Layout

```
ios/<nativeVersion>/latest.json
android/<nativeVersion>/latest.json
```

Bundle binaries live as GitHub Release assets on this repo (tags like
`ota-ios-1.0-<unix-ts>`). Each `latest.json` points at the most recent
release asset for that platform + native version.

## Branches
- `main`   → production
- `staging` → staging

## Publishing
Use `scripts/publish-ota.mjs` in the `live-react` repo. Requires:
- gh CLI authenticated (`gh auth login`)
- git push access to this repo
