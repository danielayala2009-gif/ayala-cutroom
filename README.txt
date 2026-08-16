AYALA CUTROOM v1.2 — LARGE-FILE MOUNTED EXPORT ENGINE

Upload all 6 files in this folder to the ROOT of the existing ayala-cutroom GitHub repository.

WHAT CHANGED
- Upgrades Cutroom from ffmpeg.wasm 0.11 to the 0.12 API.
- Uses WORKERFS to MOUNT each original File for reading instead of first copying the entire source video into FFmpeg's in-memory filesystem.
- Renders each kept section separately, then joins the reduced pieces.
- Unmounts the original source immediately after its clip is rendered.
- Deletes temporary parts after each join.
- Keeps Standard 720p, Small 540p, Ultra Small 360p, MP3, narration, trimming, internal cuts, clip reordering, preview, and project JSON.
- Original source files remain untouched.

WHY
The v1.0/v1.1 export failures occurred while Safari was processing multi-minute source files. v1.2 specifically targets the large input-file memory duplication that occurs when a browser copies a File into the WebAssembly filesystem.

AFTER DEPLOYMENT
1. Wait for GitHub Pages to turn green.
2. Hard-refresh the live site (Command+Shift+R).
3. Confirm the footer says v1.2.
4. Load the same two test videos.
5. Try Small MP4 first. If needed, try Ultra Small.

Note: Browser-based FFmpeg is still constrained by each browser's WebAssembly memory behavior. v1.2 materially reduces input-memory pressure but cannot remove browser limits completely.
