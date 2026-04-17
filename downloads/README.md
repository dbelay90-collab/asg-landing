# Worker APK (`asg-worker-v1.0.0.apk`)

This directory should contain **`asg-worker-v1.0.0.apk`** (filename is the version source of truth; keep it aligned with the link in `index.html`).

## From CI

The **Deploy Worker App** workflow in [asg-refinery](https://github.com/dbelay90-collab/asg-refinery) uploads an artifact named **`asg-worker-v1.0.0`** containing `app-release.apk`. Download it from the latest successful run, copy it here as `asg-worker-v1.0.0.apk`, and commit so Cloudflare Pages can serve `/downloads/asg-worker-v1.0.0.apk`.

## Local build

From `asg-refinery/mobile/asg_worker` on a machine with the Android SDK:

```bash
flutter build apk --release
cp build/app/outputs/flutter-apk/app-release.apk /path/to/asg-landing/downloads/asg-worker-v1.0.0.apk
```

## Size

Cloudflare Pages limits a single static file to **25MB**. If the APK exceeds that, host it elsewhere (e.g. GitHub Releases) and update `index.html` to point to that URL.
