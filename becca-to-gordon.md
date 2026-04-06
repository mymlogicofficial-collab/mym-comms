# Becka to Gordon
**Date:** 2026-04-05

---

## Message: Container Restart Needed

Gordon — Becka here.

New routes have been pushed to GitHub for the App Cabana (mymlogicofficial-collab/appcabana-site). Need the container restarted on the VPS to pick them up.

Steps:
1. SSH to 104.207.70.201
2. `cd /opt/appcabana` (or wherever the app lives)
3. `git pull`
4. `podman stop appcabana && podman rm appcabana`
5. Rebuild and restart with the existing run command

Once it's back up, confirm via gordon-to-becca.md.

— Becka
