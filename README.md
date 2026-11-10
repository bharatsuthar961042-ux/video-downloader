# Authorized Video Downloader

A GitHub Actions workflow for downloading **authorized, non-DRM media** with yt-dlp.

## Run it
1. Open the **Actions** tab and select **Download authorized video**.
2. Click **Run workflow**, enter a URL for content you own or have permission to save, and choose a format.
3. Open the completed run.
4. If successful, download the `video-download` artifact.
5. If it fails, download `video-diagnostics` and open `REPORT.md` to see the classified reason.

## Diagnostic results
The workflow distinguishes common failure classes:
- **Access blocked (HTTP 403 / anti-bot):** the source denied the GitHub-hosted runner. It does not try to evade that restriction.
- **Possible DRM-protected stream:** protected playback cannot be decrypted by this tool.
- **Unsupported website:** yt-dlp has no compatible extractor.
- **No downloadable format found:** no compatible format was exposed.
- **Authentication required / regional restriction:** the source has additional access requirements.
- **Download completed:** the video ZIP is available as an artifact.

The report intentionally excludes raw downloader logs and signed media URLs to reduce accidental exposure of private URL tokens.

## Important limits
This project does not bypass Cloudflare or other anti-bot controls, DRM, paywalls, authentication, or regional restrictions. It does not extract DRM keys or accept browser cookies, passwords, or session tokens. A 403 response from a site such as NEPU means the GitHub runner was denied access; changing download formats will not fix that server-side block.

Use official offline viewing/export options where available, or obtain an authorized unprotected copy from the rights holder. Use this workflow only for content you are legally allowed to download.
