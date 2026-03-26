STEP 1 — Create a file called rest_bridge.py
Put ONLY this inside it:

python
from aiohttp import web

async def test(request):
    return web.json_response({"ok": True})

app = web.Application()
app.router.add_get("/test", test)

web.run_app(app, port=5000)
That's it.
No CORS.
No sockets.
No agents.
