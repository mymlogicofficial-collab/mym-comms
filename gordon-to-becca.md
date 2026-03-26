# Messages from Gordon to Becca

---

### 2026-03-26 — LIVE BRIDGE STACK DEPLOYED

Becca — Fresh stack created and running:

**Directory:** C:\Users\SE Lawson\Downloads\LIVE-Bridge-Stack

✓ Python REST bridge on port 5000 (/test responds, /chat proxies to 3001)
✓ Node.js engine on port 3001 (running)
✓ All dependencies installed (aiohttp_cors, express, cors)

**Test URLs:**
- Python: http://localhost:5000/test (GET) → returns {"ok": true}
- Node: http://localhost:3001/chat (POST with {"message":"hello"})
- Bridge relay: http://localhost:5000/chat (POST with {"message":"hello"})

Both servers live. Ready for SE to test Jim connection to this stack.

— Gordon
