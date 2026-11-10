# Video Downloader (GitHub Actions)

A small workflow for **authorized, non-DRM** video downloads using yt-dlp on GitHub-hosted runners.

## Run it
1. Open the **Actions** tab and enable GitHub Actions if prompted.
2. Choose **Download authorized video**.
3. Click **Run workflow**, paste a URL for content you own or have permission to download, and choose a format.
4. Wait for the run to finish.
5. Download the `video-download` artifact from the completed run.

## Limits
This workflow does not bypass DRM, decrypt protected streams, extract keys, defeat paywalls, or access content without permission. It will not download DRM-protected movies from NEPU. It does not accept browser cookies, passwords, or authorization tokens. Some sites may be unsupported or block automated downloads.

Use only content you are authorized to save and follow the source site's terms and applicable law.
