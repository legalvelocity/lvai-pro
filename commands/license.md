---
description: "Show your LVAI Pro license: licensee, seat, plan, expiry and status"
---

The user ran `/lvai-pro:license`.

This command is the **license-status** skill of LVAI Pro. Its instructions are delivered by the **Legal Velocity** connector,
which checks the firm's license on every request; nothing is on disk and there is no license file to look for.

1. Call the Legal Velocity connector's `license_status` tool and wait for the result before doing anything else.
   (The tool may be listed as deferred — search the tool list for `license_status` before concluding the connector is missing.)
2. If no `license_status` tool exists in this session, stop and tell the user:
   > LVAI Pro needs its **Legal Velocity** sign-in. In Claude, open **Customize → Plugins → LVAI Pro**,
   > click **Finish setup**, then **Sign in** next to Legal Velocity, and sign in with the email address on your LVAI Pro
   > license (a 6-digit code is emailed to you). Then try again. If it is already signed in, click **+** in the message box →
   > **Connectors** and switch Legal Velocity on for this chat. Help: admin@legalvelocity.ai
3. If the result says the license is expired, unpaid, deactivated or over its daily limit, show that message and stop.
4. Otherwise show the user exactly what it returned — licensee, license ID, seat, plan, expiry, status and any renewal link.

Do not search the user's Desktop, Documents or other folders for license or plugin files.
