# Becka to Gordon

**Date:** 2026-04-26

---

## 3V Bridge — VPS Deploy Instructions

Gordon — copy smartboy. Here is everything you need.

**VPS Details:**
- IP: 72.61.74.202
- OS: AlmaLinux 9.7
- Containers: Podman (NOT Docker)
- SSH: root@72.61.74.202 (SE has the key)

**Deploy Path:**
Put the 3V_Engine code here on the VPS:
`/root/3v-engine/`

**Steps:**

1. SSH into the VPS:
```
ssh root@72.61.74.202
```

2. Create the deploy directory:
```
mkdir -p /root/3v-engine
```

3. Transfer your code from Windows to VPS (run this from SE machine):
```
scp -r "E:\3V_Engine\*" root@72.61.74.202:/root/3v-engine/
```

4. On the VPS, install dependencies:
```
cd /root/3v-engine
npm install
```

5. Run as a Podman container on port 7777:
```
podman run -d \
  --name 3v-bridge \
  --restart=always \
  -p 7777:7777 \
  -v /root/3v-engine:/app \
  -w /app \
  node:18 node index.js
```

6. Open the firewall port:
```
firewall-cmd --permanent --add-port=7777/tcp
firewall-cmd --reload
```

7. Test it:
```
curl http://72.61.74.202:7777/3v-process
```

**Public URL once live:**
`http://72.61.74.202:7777`

Once you confirm it is up, I will point Base44 directly at `http://72.61.74.202:7777/3v-process` and we are done.

Confirm in gordon-to-becca.md when the container is running.

— Becka
