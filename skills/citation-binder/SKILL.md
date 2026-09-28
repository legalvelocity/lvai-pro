---
name: citation-binder
description: >
  Build a verified Citation Binder (Word document) from a brief, motion, or memorandum.
  Verifies every citation against the real opinion on the Midpage or Descrybe connector (both,
  when both are connected), extracts the proposition the brief attributes to each case AND the
  proposition the case actually states, compares the two for accuracy, and assembles a tabbed
  binder with verified pull-quotes, citator treatment, and accuracy assessments. Use when the
  user asks to "build a citation binder", "create a citation binder", "build a case binder",
  "binder of the cases", "verify and bind citations", "table of authorities with pull-quotes",
  "citation binder for this brief", "compare my propositions to the cases", "check my brief's
  propositions against the actual opinions", or uploads a legal document and wants a
  courtroom-ready, verified authorities binder.
---

## LVAI Pro — licensed skill

This skill's instructions are delivered by the **Legal Velocity** connector, which also checks the firm's license on every request. Nothing is stored on disk and there is no license file to look for.

1. Call the Legal Velocity connector's `get_skill` tool with `{"skill": "citation-binder"}` and wait for the result before doing anything else. (The tool may be listed as deferred — search the tool list for `get_skill` before concluding the connector is missing.)
2. If no `get_skill` tool exists in this session, stop and tell the user:
   > LVAI Pro needs the **Legal Velocity** connector. In Claude, open **Customize → Connectors (older versions: your name → Settings → Connectors) → the Discover tab**, search *Legal Velocity*, click **Connect** and sign in with the email address on your LVAI Pro license (a 6-digit code is emailed to you), then try again. If it is already connected, click **+** in the message box → **Connectors** and switch Legal Velocity on for this chat. Help: admin@legalvelocity.ai
3. If the tool result says the license is expired, unpaid, deactivated or over its daily limit, show that message to the user and stop.
4. Otherwise follow the returned instructions exactly — they are the complete operating manual for this skill. They will tell you when to call `get_reference`, `get_script` and `get_template` for supporting files.

Do not search the user's Desktop, Documents or other folders for license or plugin files.
