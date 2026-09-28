---
name: discovery
description: >
  Generate discovery documents including interrogatories, requests for production,
  and requests for admission. Use when the user asks to "draft interrogatories",
  "create discovery requests", "write requests for production", "discovery questions",
  "draft RFPs", "create requests for admission", "generate discovery",
  "respond to interrogatories", or needs interrogatories, document requests,
  requests for admission or responses to them for divorce, custody, employment,
  personal injury, or other case types.
---

## LVAI Pro — licensed skill

This skill's instructions are delivered by the **Legal Velocity** connector, which also checks the firm's license on every request. Nothing is stored on disk and there is no license file to look for.

1. Call the Legal Velocity connector's `get_skill` tool with `{"skill": "discovery"}` and wait for the result before doing anything else. (The tool may be listed as deferred — search the tool list for `get_skill` before concluding the connector is missing.)
2. If no `get_skill` tool exists in this session, stop and tell the user:
   > LVAI Pro needs the **Legal Velocity** connector. In Claude, open **Customize → Connectors (older versions: your name → Settings → Connectors) → the Discover tab**, search *Legal Velocity*, click **Connect** and sign in with the email address on your LVAI Pro license (a 6-digit code is emailed to you), then try again. If it is already connected, click **+** in the message box → **Connectors** and switch Legal Velocity on for this chat. Help: admin@legalvelocity.ai
3. If the tool result says the license is expired, unpaid, deactivated or over its daily limit, show that message to the user and stop.
4. Otherwise follow the returned instructions exactly — they are the complete operating manual for this skill. They will tell you when to call `get_reference`, `get_script` and `get_template` for supporting files.

Do not search the user's Desktop, Documents or other folders for license or plugin files.
