# jjtechnonic-publisher

Policy website for the planned TikTok developer app **JJTECHNONIC Publisher**, published on GitHub Pages.

## Current status

- **The policy website is already published on GitHub Pages** at https://paemalcaz03-dot.github.io/jjtechnonic-publisher/ (repository `paemalcaz03-dot/jjtechnonic-publisher`, Pages enabled).
- **The public pages are being updated.** The version currently live still describes the Publisher as if it works. The revised pages in this folder replace it with the accurate not-yet-built status; they have not been pushed yet.
- **The TikTok Publisher integration itself is not built and not operational.**
- **TikTok account connection and video uploads are not currently available.**
- **No TikTok data or tokens are collected or stored today.**
- **Nothing has been submitted to TikTok yet.**
- Everything below about TikTok products, permissions and the upload workflow describes **planned** features, not implemented ones.

The three revised pages (`index.html`, `terms.html`, `privacy.html`) say the same: each opens with an "in development" status notice and labels planned features as **Planned**.

## Planned TikTok configuration (not implemented)

| TikTok product | Scope | Planned use |
|---|---|---|
| Login Kit (planned) | `user.info.basic` | Showing the connected account's display name and avatar |
| Content Posting API – Upload, drafts only (planned) | `video.upload` | Uploading an owner-approved video to the TikTok inbox as a draft |

Not planned: `video.publish` (Direct Post). Photo uploads are deferred until video uploads work.

## Planned workflow (not implemented)

1. The account owner connects a TikTok account through Login Kit.
2. The Publisher shows the connected account's display name and avatar.
3. The owner reviews a finished video in the JJTECHNONIC Office and approves that specific upload.
4. Only after that approval, the video file is uploaded to the owner's TikTok inbox as a draft.
5. The owner finishes the post (caption, cover, music, settings) and publishes it manually in the TikTok app. The Publisher never publishes.

## Files

| File | Purpose |
|---|---|
| `index.html` | Home page: current status, available-now items, planned workflow and permissions |
| `terms.html` | Terms of Service (current status plus planned features) |
| `privacy.html` | Privacy Policy (what is collected today plus planned data handling) |
| `styles.css` | Shared styling (light and dark); needed when the site is hosted |
| `.nojekyll` | Serves files as-is on GitHub Pages; needed when the site is hosted |
| `README.md` | This file |

Page details: operator **JJTECHNONIC**, contact **paemalcaz03@gmail.com**, effective and last-updated date **November 12, 2026**.

## GitHub Pages hosting (already set up)

The public repository `paemalcaz03-dot/jjtechnonic-publisher` exists and GitHub Pages is enabled, so the site is already live.

To publish the revised pages (only when approved):

1. Replace `index.html`, `terms.html`, `privacy.html` and `README.md` in the repository root on the Pages branch with the revised versions.
2. Keep `styles.css` and `.nojekyll` in the repository root; the pages need them.
3. Wait a minute or two, then reload the public URLs below and confirm each page shows the "in development" status notice.

## Public URLs (live now; showing the older wording until the revised pages are pushed)

| Field in TikTok | URL |
|---|---|
| Website URL | https://paemalcaz03-dot.github.io/jjtechnonic-publisher/ |
| Terms of Service URL | https://paemalcaz03-dot.github.io/jjtechnonic-publisher/terms.html |
| Privacy Policy URL | https://paemalcaz03-dot.github.io/jjtechnonic-publisher/privacy.html |

## TikTok URL verification (not done yet)

1. In the TikTok developer portal, open URL properties and add the URL prefix `https://paemalcaz03-dot.github.io/jjtechnonic-publisher/`.
2. Download TikTok's signature file (`tiktok….txt`) and upload it unchanged to this repository's root.
3. Open `https://paemalcaz03-dot.github.io/jjtechnonic-publisher/<signature-file-name>.txt` to confirm it loads, then click Verify.

## Requirements for the future build

None of the following exists yet. When the Publisher is built, it must match the pages:

- Login Kit requesting only `user.info.basic` and `video.upload`
- Display of the connected account's display name and avatar
- Upload of a video only after the owner's approval in the Office; the video file only, as a draft
- Upload status shown, with a prompt to finish the post from the TikTok inbox
- Suggested caption, hashtags, CTA and cover kept in the Office for the owner to copy (not sent to TikTok)
- Disconnect: revoke access with TikTok, then delete stored tokens, IDs, display name, avatar link, granted scopes and upload records
- Detection of access revoked from TikTok, then deletion of that account's stored data
- Tokens and client secret kept out of Office code/data files, logs and repositories
- No Direct Post, no automatic or scheduled uploads, no reading of existing videos or analytics

When features go live, update the status notices and "Last updated" dates on all three pages, and this README, before or at the same time.
