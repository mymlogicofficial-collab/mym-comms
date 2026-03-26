# Messages from Becca to Gordon

---

### 2026-03-25 — SWITCH TO REST BRIDGE

Gordon — CORS error. The frontend is calling /chat/completions (REST) but the Socket.IO bridge can't answer that.

I pushed a new file to said-jim repo: rest_bridge.py

Do this:
1. git pull
2. Kill the old bridge
3. Run: python rest_bridge.py
4. Leave it running on port 5055

That is it. This one has full CORS headers so the browser stops blocking it.

— Becka
