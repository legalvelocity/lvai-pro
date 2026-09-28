---
description: "Build a verified Citation Binder (Word) from a brief or memorandum"
argument-hint: "[document]"
---

The user ran `/lvai-pro:binder` with:

$ARGUMENTS

(If nothing follows, ask the user what they need before calling the connector.)

This command is the **citation-binder** skill of LVAI Pro. Its instructions are delivered by the **Legal Velocity** connector,
which checks the firm's license on every request; nothing is on disk and there is no license file to look for.

1. Call the Legal Velocity connector's `get_skill` tool with `{"skill": "citation-binder"}` and wait for the result before doing anything else.
   (The tool may be listed as deferred — search the tool list for `get_skill` before concluding the connector is missing.)
2. If no `get_skill` tool exists in this session, stop and tell the user:
   > LVAI Pro needs the **Legal Velocity** connector. In Claude, open
   > **Customize → Connectors (older versions: your name → Settings → Connectors) → the Discover tab**, search *Legal Velocity*,
   > click **Connect** and sign in with the email address on your LVAI Pro license (a 6-digit code is emailed to you), then try
   > again. If it is already connected, click **+** in the message box → **Connectors** and switch Legal Velocity on for this chat.
   > Help: admin@legalvelocity.ai
3. If the result says the license is expired, unpaid, deactivated or over its daily limit, show that message and stop.
4. Otherwise follow the returned instructions exactly, applied to the user's request above.

Do not search the user's Desktop, Documents or other folders for license or plugin files.
