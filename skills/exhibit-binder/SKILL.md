---
name: exhibit-binder
description: >
  Merge a set of exhibits (PDF, Word, images) into ONE court-ready PDF binder: caption cover page, Exhibit Index with
  page references, a tab page before every exhibit ("EXHIBIT A"), bookmarks, "Page X of Y" on every page and optional
  Bates numbers. Use when the user asks to "create an exhibit binder", "merge the exhibits", "combine these PDFs into one",
  "make one PDF of all the exhibits", "tab the exhibits", "exhibit list", "exhibit index", "Bates stamp the exhibits",
  "put the exhibits together for the motion", "appendix of exhibits", or has a folder of exhibit files that must go to
  the court or the other side as a single document. Works entirely on the user's computer — nothing is uploaded.
---

## LVAI Pro — licensed skill

This skill's instructions are delivered by the **Legal Velocity** connector, which also checks the firm's license on every request. Nothing is stored on disk and there is no license file to look for.

1. Call the Legal Velocity connector's `get_skill` tool with `{"skill": "exhibit-binder"}` and wait for the result before doing anything else. (The tool may be listed as deferred — search the tool list for `get_skill` before concluding the connector is missing.)
2. If no `get_skill` tool exists in this session, stop and tell the user:
   > LVAI Pro needs the **Legal Velocity** connector. In Claude, open **Customize → Connectors (older versions: your name → Settings → Connectors) → the Discover tab**, search *Legal Velocity*, click **Connect** and sign in with the email address on your LVAI Pro license (a 6-digit code is emailed to you), then try again. If it is already connected, click **+** in the message box → **Connectors** and switch Legal Velocity on for this chat. Help: admin@legalvelocity.ai
3. If the tool result says the license is expired, unpaid, deactivated or over its daily limit, show that message to the user and stop.
4. Otherwise follow the returned instructions exactly — they are the complete operating manual for this skill. They will tell you when to call `get_reference`, `get_script` and `get_template` for supporting files.

Do not search the user's Desktop, Documents or other folders for license or plugin files.
