# CaptionFlow AI

Free, watermark-free auto-captions for reels. Everything runs **in your browser** (no backend, no account, no API key).

- **Speech recognition:** Whisper (open source) via Transformers.js, loaded from the jsDelivr CDN. The model downloads from Hugging Face the first time you press *Generate captions* (Tiny ~40 MB, Base ~80 MB, Small ~250 MB) and is cached afterwards. Auto-detects language (English, Urdu, Hindi, etc.) and does not translate.
- **Export:** every frame (video + styled/animated captions) is drawn to a canvas and recorded with the original audio. No watermark, no limits.

## Deploy on GitHub Pages
1. github.com → **New repository** → name it `captionflow` → Public → Create.
2. **Add file → Upload files** → upload `index.html` and `README.md` → Commit.
3. **Settings → Pages** → Source: *Deploy from a branch* → Branch: `main`, folder `/ (root)` → Save.
4. After ~1 minute your site is at `https://YOUR-USERNAME.github.io/captionflow/`.

GitHub Pages only hosts static files; this app needs no server, so nothing else is required.

## Limits (be aware)
- Export runs in **real time** (a 30 s reel takes ~30 s) and the tab must stay visible.
- Output is MP4 if your browser can record it (Safari/recent Chrome), otherwise WebM. WebM from browsers may not show duration/seek bar in some players; re-save through any converter if needed.
- Quality never exceeds the source; "1080p" is capped to the source size.
- Whisper can occasionally invent text over silence/music: delete those captions in the editor.
- Use desktop Chrome/Edge for best speed (WebGPU). Phones may run out of memory with the Small model.
- Fonts are system fonts (Arial Black/Impact fallbacks) — no font licensing issues; Urdu uses your system's Arabic-script font.
