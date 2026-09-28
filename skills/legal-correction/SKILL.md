---
name: legal-correction
description: >
  Auto-correct a legal document based on a Citation Verification Report,
  then re-verify the corrected document. Use when the user asks to
  "fix the citations", "correct the brief per the report", "apply the
  verification fixes", "fix the issues the verification report found",
  "narrow the holdings", "make the corrections from the report", or has
  just run /verify and wants the flagged citations actually fixed in the
  document. This is the natural follow-on to /verify — it reads the
  verification report's manifest, rewrites flagged passages of the brief
  to align with the verified case language, and runs a new verification
  check on the corrected document. Not for general editing requests.
---

## LVAI Pro — licensed skill

This skill's instructions are delivered by the **Legal Velocity** connector, which also checks the firm's license on every request. Nothing is stored on disk and there is no license file to look for.

1. Call the Legal Velocity connector's `get_skill` tool with `{"skill": "legal-correction"}` and wait for the result before doing anything else. (The tool may be listed as deferred — search the tool list for `get_skill` before concluding the connector is missing.)
2. If no `get_skill` tool exists in this session, stop and tell the user:
   > LVAI Pro needs the **Legal Velocity** connector. In Claude, open **Customize → Connectors (older versions: your name → Settings → Connectors) → the Discover tab**, search *Legal Velocity*, click **Connect** and sign in with the email address on your LVAI Pro license (a 6-digit code is emailed to you), then try again. If it is already connected, click **+** in the message box → **Connectors** and switch Legal Velocity on for this chat. Help: admin@legalvelocity.ai
3. If the tool result says the license is expired, unpaid, deactivated or over its daily limit, show that message to the user and stop.
4. Otherwise follow the returned instructions exactly — they are the complete operating manual for this skill. They will tell you when to call `get_reference`, `get_script` and `get_template` for supporting files.

Do not search the user's Desktop, Documents or other folders for license or plugin files.
