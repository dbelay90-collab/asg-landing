# ASG Worker App Downloads

The Android APK is hosted on GitHub Releases in the public
[asg-releases](https://github.com/dbelay90-collab/asg-releases) repo.

The source code repo (asg-refinery) is private — release binaries are
published to asg-releases so workers can download without GitHub access.

**Current release:** v1.0.0

**Download URL:**
https://github.com/dbelay90-collab/asg-releases/releases/download/v1.0.0/asg-worker-v1.0.0.apk

## Updating the APK

When a new version is built:

1. Build the APK via CI (Deploy Worker App workflow in asg-refinery)
2. Download the artifact from GitHub Actions
3. Create a new GitHub Release on asg-releases:

   ```bash
   gh release create v1.x.x path/to/asg-worker-v1.x.x.apk \
     -R dbelay90-collab/asg-releases \
     --title "ASG Worker v1.x.x" \
     --notes "Release notes here"
   ```

4. Update the download URL in `index.html` if the version tag changed

## Why a Separate Public Repo?

- asg-refinery is private (protects source code)
- GitHub Releases on private repos return 404 for unauthenticated users
- asg-releases is public — anyone can download release binaries
- Cloudflare Pages has a 25MB per-file limit — APK is ~50MB

## Version History

| Version | Date       | Release |
|---------|------------|---------|
| v1.0.0  | 2026-04-17 | [GitHub](https://github.com/dbelay90-collab/asg-releases/releases/tag/v1.0.0) |
