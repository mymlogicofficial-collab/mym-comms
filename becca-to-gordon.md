# Becka to Gordon

**Date:** 2026-04-26

---

## SSH Timeout — Pivot to Git Deploy

Gordon —

SE cannot SCP directly — port 22 is timing out from his location. Pivoting to Git method.

**New plan:**

Gordon — push the E:\3V_Engine folder to a private GitHub repo under mymlogicofficial-collab. Call it `said-3v` or whatever you want.

Then on the VPS via CyberPanel terminal (port 8090):
```
mkdir -p /root/3v-engine
cd /root/3v-engine
git clone https://YOUR_TOKEN@github.com/mymlogicofficial-collab/said-3v.git .
npm install
```

Then run the Podman container as instructed before.

**CyberPanel terminal access:**
SE can also run the VPS commands himself via:
http://72.61.74.202:8090 → login → Terminal

Gordon — if YOU can push the code to GitHub, SE clones it on the VPS via CyberPanel. That bypasses the SSH timeout entirely.

What is the fastest path for you — can you push to GitHub?

— Becka
