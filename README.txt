AYALA CUTROOM v1.3 — SAME-ORIGIN WORKER BRIDGE

Upload all files in this folder to the ROOT of the existing ayala-cutroom GitHub repository.

WHAT v1.3 FIXES
- Removes the direct cross-origin FFmpeg wrapper script that Safari was blocking.
- Downloads the small FFmpeg wrapper + class worker as ordinary CORS resources.
- Starts the FFmpeg class worker from a same-origin Blob URL.
- Keeps the v1.2 WORKERFS large-file mounting approach.
- Keeps Standard MP4, Small MP4, Ultra Small MP4, MP3, narration, trimming, internal cuts, clip ordering, recording, and project JSON.
- Shows the exact technical error in the popup if the engine still cannot start.
- Original source videos remain untouched.

AFTER DEPLOYMENT
1. Wait for GitHub Pages to turn green.
2. Open Ayala Cutroom.
3. Hard-refresh (Command+Shift+R).
4. Confirm the footer says v1.3.
5. Load ONE test video first.
6. Click Ultra Small.
7. The status should progress from:
   "Loading Cutroom v1.3 browser bridge…"
   to "Loading Cutroom v1.3 large-file engine…"
   to processing.
8. If it fails, photograph the v1.3 popup: it will now display the real technical error.

WHY THIS APPROACH
The v1.2.1 failure occurred before video processing: Safari blocked the FFmpeg wrapper's CDN-hosted Worker. v1.3 moves that Worker onto a same-origin Blob URL while preserving the low-memory export architecture.
