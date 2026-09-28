---
name: license-status
description: >
  Show the user's own LVAI Pro / Legal Velocity license: who it is licensed to, license ID, seat, plan,
  expiry date, days left and status. Use when the user says "check my LVAI Pro license status", "check my
  license", "is my LVAI Pro license active", "when does my license expire", "LVAI Pro license status",
  "Legal Velocity license", "verify my license", "is my subscription active", "manage my LVAI Pro
  subscription", or asks anything about their own LVAI Pro license or renewal. This is a read-only check
  through the Legal Velocity connector; it needs no folder, no file and no admin tool.
---

## LVAI Pro — license status

1. Call the Legal Velocity connector's `license_status` tool with `{}` (no arguments). The tool may be listed as
   deferred — search the tool list for `license_status` before concluding the connector is missing.
2. Show the user exactly what it returns (licensed to, license ID, seat, plan, expiry, status, and any renewal or
   billing link it includes). Do not add, guess or look up anything else.
3. If no `license_status` tool exists in this session, tell the user:
   > LVAI Pro needs the **Legal Velocity** connector. In Claude, open
   > **Customize → Connectors (older versions: your name → Settings → Connectors) → the Discover tab**, search *Legal Velocity*,
   > click **Connect** and sign in with the email address on your LVAI Pro license (a 6-digit code is emailed to you), then try
   > again. If it is already connected, click **+** in the message box → **Connectors** and switch Legal Velocity on for this chat.
   > Help: admin@legalvelocity.ai

Never search the user's folders for license files, and never ask for a server folder or an admin key — those belong
to the vendor's separate administration plugin, not to the user's license check.
