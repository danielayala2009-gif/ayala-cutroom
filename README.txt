AYALA CUTROOM v1.1 — LOW-MEMORY EXPORT UPDATE

Upload all files in this folder to the ROOT of the existing ayala-cutroom GitHub repository.

v1.1 fixes the real-world export failure found with two multi-minute class videos:
- Processes ONE source clip at a time.
- Deletes source data from the FFmpeg virtual filesystem as soon as each clip is rendered.
- Removes multiple marked middle sections in a single render pass per clip.
- Joins clips incrementally and deletes intermediates.
- Adds an Ultra Small 360p export preset for tight memory/upload limits.
- Keeps Standard 720p, Small 540p, MP3, narration, trimming, internal cuts, reordering, and project JSON.

IMPORTANT
After GitHub Pages redeploys, hard-refresh the site (Command+Shift+R on Mac).
If installed as a PWA, close/reopen it after deployment so the new service worker updates.
