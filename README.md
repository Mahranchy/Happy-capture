# HappyCapture (Web)

Browser version of HappyCapture — smile-triggered photo + short video capture,
on-device face detection, smart zoom, and colour grading.

## Live app
Replace this line with your Pages URL after deploying:
`https://YOUR-USERNAME.github.io/happycapture/`

## Features
- Smile detection via MediaPipe Face Landmarker (on-device, no uploads)
- Smart digital zoom toward the largest face (up to 2.5×)
- Auto photo + 4s clip on smile
- Manual photo and video buttons
- FX presets: Off / Light / Strong (brightness, contrast, saturation, sepia, vignette, sharpening)
- Auto night boost in low light
- Timestamp watermark
- Session gallery with iOS share sheet saving

## How to run
1. Open the live URL in Safari on iPhone.
2. Allow camera + microphone when prompted.
3. Optional: Share → Add to Home Screen.

Camera access requires HTTPS, so the file must be hosted
(GitHub Pages, Netlify, or Cloudflare Pages all work, free).

## Deploy on GitHub Pages
1. Create a public repo, upload `index.html`.
2. Repo → Settings → Pages → Source: Deploy from a branch → main / root → Save.
3. Wait ~1–2 min. Your URL appears in the green box.

## Tuning
Edit the constants at the top of the `<script>` in `index.html`:

| Constant | Default | Effect |
|---|---|---|
| `SMILE_THRESHOLD` | 0.42 | Raise to make detection stricter |
| `CORNER_LIFT` | 0.012 | Raise to require a stronger smile |
| `CLIP_MS` | 4000 | Auto-clip length in ms |
| `ZOOM_MAX` | 2.5 | Maximum digital zoom |
| `SHOW_TIMESTAMP` | true | Toggle watermark |

## Known iOS limitations
- Auto-save on smile is blocked by iOS Safari; captures land in the
  on-screen gallery — tap a thumbnail to save to Photos.
- Video grading on iOS Safari < 17 may be skipped.
- The tab must stay open; there is no background capture in a browser.

## License
Personal use.