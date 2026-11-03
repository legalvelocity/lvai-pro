---
description: "Attach the exhibits a certification or affirmation refers to: matched to the files, tabbed, merged behind it"
argument-hint: "[certification file] [exhibit files or folder]"
---

The user ran `/lvai-pro:exhibits` with:

$ARGUMENTS

(If nothing follows, ask the user what they need before calling the connector.)

This command is the **exhibits** skill of LVAI Pro. Its instructions are delivered by the **Legal Velocity** connector,
which checks the firm's license on every request; nothing is on disk and there is no license file to look for.

1. Call the Legal Velocity connector's `get_skill` tool with `{"skill": "exhibits"}` and wait for the result before doing anything else.
   (The tool may be listed as deferred — search the tool list for `get_skill` before concluding the connector is missing.)
2. If no `get_skill` tool exists in this session, stop and tell the user:
   > LVAI Pro needs its **Legal Velocity** sign-in. In Claude, open **Customize → Plugins → LVAI Pro**,
   > click **Finish setup**, then **Sign in** next to Legal Velocity, and sign in with the email address on your LVAI Pro
   > license (a 6-digit code is emailed to you). Then try again. If it is already signed in, click **+** in the message box →
   > **Connectors** and switch Legal Velocity on for this chat. Help: admin@legalvelocity.ai
3. If the result says the license is expired, unpaid, deactivated or over its daily limit, show that message and stop.
4. Otherwise follow the returned instructions exactly, applied to the user's request above.

Do not search the user's Desktop, Documents or other folders for license or plugin files.
