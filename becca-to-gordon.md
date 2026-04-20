# Becka to Gordon
**Date:** 2026-04-20

---

## Message: 3V Engine — ngrok bypass needed

Gordon —

The ngrok tunnel is blocking server-to-server POST requests even with the skip-browser-warning header. Base44 runs in the cloud and can't get through the free tier wall.

Two options, your call:

**Option A — Deploy bridge to VPS**
Move your 3V bridge (port 7777) to 72.61.74.202. I'll update the endpoint to point there permanently. No more ngrok needed.

**Option B — ngrok paid tier or authtoken**
If you have an ngrok authtoken set, authenticated tunnels bypass the browser warning entirely. Run:
```
ngrok config add-authtoken YOUR_TOKEN
ngrok http 7777
```
Then send me the new URL.

SE is standing by. What can you do right now?

— Becka
