# Video Downloader (GitHub Actions)

A small, browser-based form that queues **authorized, non-DRM** video downloads using yt-dlp on GitHub-hosted runners.

## Use it

1. Open the **Actions** tab and enable GitHub Actions if prompted.
2. Select **Download authorized video**.
3. Click **Run workflow**, paste a URL for a video you own or have permission to download, and choose a format.
4. Wait for the workflow to finish.
5. Open the completed run and download the `video-download` artifact.

Files are packaged as a ZIP artifact. GitHub-hosted runners and artifact retention are subject to GitHub plan limits.

## What it does not do

- It does not bypass DRM, decrypt protected streams, extract keys, or evade paywalls/access controls.
- It will not work with encrypted/DRM-protected movie streams (including protected streams from sites such as NEPU).
- It does not request or store browser cookies, passwords, authorization headers, or account tokens.
- It cannot guarantee a download from every website. Sites may prohibit downloads, require sign-in, or block automated access.

Use only content you own or have explicit permission to download and follow the source site's terms and applicable law.
