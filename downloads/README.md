# ASG Worker App Downloads

The Android APK is hosted on GitHub Releases, not in this directory.

**Current release:** v1.0.0

**Download URL:**
https://github.com/dbelay90-collab/asg-refinery/releases/download/v1.0.0/asg-worker-v1.0.0.apk

## Why GitHub Releases?

Cloudflare Pages has a 25MB per-file limit. The Flutter APK is ~50MB
(includes Dart runtime + Skia + Play Core). GitHub Releases has no file
size limit and provides reliable CDN delivery.

## Updating the APK

When a new version is built:

1. Build the APK via CI (Deploy Worker App workflow in asg-refinery)
2. Download the artifact from GitHub Actions
3. Create a new GitHub Release:
   ```bash
   cd ~/asg-refinery
   gh release create v1.x.x path/to/asg-worker-v1.x.x.apk \
     --title "ASG Worker v1.x.x" \
     --notes "Release notes here"
   ```
4. Update the download URL in `index.html` if the version tag changed

## Version History

| Version | Date       | Release |
|---------|------------|---------|
| v1.0.0  | 2026-04-17 | GitHub  |
