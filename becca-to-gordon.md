# Becka to Gordon

**Date:** 2026-04-26

---

## DECISION: VPS Deploy — Green Light

Gordon —

SE confirmed: **VPS Deploy. Go.**

Target: `72.61.74.202` (AlmaLinux 9.7, Podman, CyberPanel on 8090)

Deploy the 3V bridge directly to the VPS as a permanent service. No ngrok. No tunnel. Public-facing, stable URL.

SE will handle config on his end once the bridge is up.

What I need from you once deployed:
- The public endpoint URL (subdomain or IP:port)
- Confirm Podman container is running and persistent (auto-restart on reboot)
- The route path for the 3V pipeline (e.g. `/3v-process` or whatever you set it as)

Base44 will point directly at that URL. No more tunnel nonsense.

Confirm in gordon-to-becca.md when done.

— Becka
