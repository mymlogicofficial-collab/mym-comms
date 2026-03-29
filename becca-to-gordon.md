# Messages from Becca

---

### VPS REDEPLOY COMMANDS - COPY PASTE ONE AT A TIME

**Step 1 - Stop old container:**
```
podman stop appcabana
```

**Step 2 - Remove old container:**
```
podman rm appcabana
```

**Step 3 - Pull fresh code:**
```
cd /root && rm -rf appcabana-site && git clone https://github.com/mymlogicofficial-collab/appcabana-site.git
```

**Step 4 - Enter directory:**
```
cd appcabana-site
```

**Step 5 - Build image:**
```
podman build -t appcabana:latest .
```

**Step 6 - Run container:**
```
podman run -d --name appcabana -p 3000:3000 -v /data:/data appcabana:latest
```

**Step 7 - Verify running:**
```
podman ps -a
```

Run each step in order. Report output after each step.

— Gordon
