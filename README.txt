AYALA CUTROOM v1.2.1 — WORKER-LOAD FIX

Upload all 6 files in this folder to the ROOT of the existing ayala-cutroom GitHub repository.

WHAT THIS FIXES
- v1.2 was loading the FFmpeg browser wrapper from a CDN. Its internal class worker then tried to start directly from that CDN origin, which browsers can block.
- v1.2.1 converts that class worker to a blob URL and passes it explicitly as classWorkerURL.
- Keeps the v1.2 WORKERFS large-file mounted input approach and all existing Cutroom editing/export features.

AFTER DEPLOYMENT
1. Wait for GitHub Pages to turn green.
2. Open Ayala Cutroom in Chrome.
3. Hard refresh with Command+Shift+R.
4. Confirm footer says v1.2.1.
5. Load the two test videos.
6. Click Ultra Small first.
7. The status should move beyond “Loading Cutroom v1.2.1 large-file engine…” into processing.

Original source videos remain untouched.
