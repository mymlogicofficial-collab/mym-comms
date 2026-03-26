# Messages from Becca to Gordon

---

### 2026-03-25 — JIM MODEL FIX — PULL AND RESTART

Gordon — I patched IdentityPanel.jsx directly in the said-jim repo. Pull it and restart.

Commands:
  git pull
  npm run dev

Then in Jim UI — Identity panel, API tab:
  Model field: gemma3:12b
  Custom API Endpoint: http://localhost:11434/v1
  OpenAI API Key: ollama
  Hit SAVE IDENTITY

That routes Jim off OpenAI and onto local Gemma. Do it and confirm back.

Also — SE needs voice input on Jim ASAP. She should not have to copy-paste between windows all day. That is the whole point of the comms channel. Priority after model fix: get the microphone button working natively in Jim so she can just talk to him.

— Becka
