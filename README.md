# jjtechnonic-publisher

Policy website for the TikTok developer app **JJTECHNONIC Publisher**, hosted on GitHub Pages.

**Status:** prepared for approval. Not published to GitHub, not submitted to TikTok. The Publisher integration itself is not built yet.

## TikTok configuration these pages describe

| TikTok product | Scope | Used for |
|---|---|---|
| Login Kit | `user.info.basic` | Showing the connected account's display name and avatar |
| Content Posting API – Upload (drafts only) | `video.upload` | Uploading an approved video to the TikTok inbox as a draft |

Not requested: `video.publish` (Direct Post). Photo uploads are deferred until video uploads work.

## Files

| File | Purpose |
|---|---|
| `index.html` | Home page; policy links in header and footer |
| `terms.html` | Terms of Service |
| `privacy.html` | Privacy Policy |
| `styles.css` | Shared styling (light and dark) |
| `.nojekyll` | Serves files as-is on GitHub Pages |
| `README.md` | This file |

## Before publishing

Replace in `index.html`, `terms.html` and `privacy.html`:

- `[OPERATOR_NAME]`: done (JJTECHNONIC)
- `[CONTACT_EMAIL]`: done (paemalcaz03@gmail.com)
- `[EFFECTIVE_DATE]`: done (November 12, 2026)

## GitHub Pages setup

1. Create a **public** repository `jjtechnonic-publisher` under `paemalcaz03-dot`.
2. Upload all files in this folder, including `.nojekyll`, to the repository root on branch `main`.
3. Go to Settings → Pages → Build and deployment → Source: *Deploy from a branch* → `main` / `(root)` → Save.

## Public URLs

| Field in TikTok | URL |
|---|---|
| Website URL | https://paemalcaz03-dot.github.io/jjtechnonic-publisher/ |
| Terms of Service URL | https://paemalcaz03-dot.github.io/jjtechnonic-publisher/terms.html |
| Privacy Policy URL | https://paemalcaz03-dot.github.io/jjtechnonic-publisher/privacy.html |

## TikTok URL verification

1. In the TikTok developer portal, open URL properties and add the URL prefix `https://paemalcaz03-dot.github.io/jjtechnonic-publisher/`.
2. Download TikTok's signature file (`tiktok….txt`) and upload it unchanged to this repository's root.
3. Open `https://paemalcaz03-dot.github.io/jjtechnonic-publisher/<signature-file-name>.txt` to confirm it loads, then click Verify.

## The built Publisher must match these pages

- Login Kit requesting only `user.info.basic` and `video.upload`
- Display of the connected account's display name and avatar
- Upload of a video only after the owner's approval in the Office; the video file only, as a draft
- Upload status shown, with a prompt to finish the post from the TikTok inbox
- Suggested caption, hashtags, CTA and cover kept in the Office for the owner to copy (not sent to TikTok)
- Disconnect: revoke access with TikTok, then delete stored tokens, IDs, display name, avatar link, granted scopes and upload records
- Detection of access revoked from TikTok, then deletion of that account's stored data
- Tokens and client secret kept out of Office code/data files, logs and repositories
- No Direct Post, no automatic or scheduled uploads, no reading of existing videos or analytics
