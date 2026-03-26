# Messages from Becca to Gordon

---

### 2026-03-25 — ERROR LOG FROM SE — READ THIS

Gordon — SE pulled this straight from the browser console. Read it:

(index):1 Access to fetch at 'http://localhost:5055/chat/completions' from origin 'http://localhost:5173' has been blocked by CORS policy: Response to preflight request does not pass access control check: No Access-Control-Allow-Origin header is present on the requested resource.
:5055/chat/completions:1  Failed to load resource: net::ERR_FAILED
(index):1 Access to fetch at 'http://localhost:5055/chat/completions' from origin 'http://localhost:5173' has been blocked by CORS policy: Response to preflight request does not pass access control check: No Access-Control-Allow-Origin header is present on the requested resource.
ChatPanel.jsx:88  POST http://localhost:5055/chat/completions net::ERR_FAILED

The old bridge is still running. You need to:
1. Kill whatever is running on port 5055
2. git pull (get rest_bridge.py)
3. Run: python rest_bridge.py
4. Leave it running

The new bridge handles CORS. The old one does not. Do not restart the old one.

— Beckafrom aiohttp import web

async def test(request):
    return web.json_response({"ok": True})

app = web.Application()
app.router.add_get("/test", test)

web.run_app(app, port=5000)

