# LVAI Pro

The complete Legal Velocity AI platform for Claude — legal research and citation verification on **Midpage** or
**Descrybe** (whichever connector you have), NJ/NY real estate transaction management, and intelligent PDF form filling.

## Slash commands

Type `/` in Claude and pick one — or say what you need in plain words; the skills trigger either way.
`/lvai-pro:research`, `/deep-research`, `/verify`, `/correct`, `/draft`, `/case-summary`, `/discovery`, `/binder`, `/hyperlink`, `/exhibit-binder`, `/exhibits`,
`/fill-form`, `/analyze-form`, `/extract-data`, `/intake`, `/calendar-dates`, `/prepare-rider`, `/closing-docs`, `/title-review`, `/license`.

## How it works

This plugin is the same for every customer and contains only the skill names and the phrases that trigger them.
The skills themselves — instructions, checklists, templates and build scripts — are delivered on demand by the
**Legal Velocity** connector, which checks your firm's license on every request. Renewals happen on our side.
Most updates reach you automatically through the connector; when a release adds a command, the update email says so and the plugin updates from Claude's directory (or with the download link in that email).

## What this plugin runs, sends and fetches

- It contains no code of its own: only skill and command files (Markdown) and a reference to the Legal Velocity connector at `https://mcp.legalvelocity.ai/mcp` (`.mcp.json`).
- Every skill calls that connector's read-only tools — `get_skill`, `get_reference`, `get_script`, `get_template`, `license_status` — which return the skill's instructions, reference files, build scripts (Python/shell, run locally in your Cowork session on the files you give it) and document templates under your license. The connector receives the name of the skill or file requested, never the content of your conversation or documents.
- The research skills also use the legal-research connector you connected yourself (Midpage or Descrybe), and the calendaring skill your calendar connector. Nothing is sent anywhere else.

## Skills

| Skill | What it does |
|-------|--------------|
| `case-summary` | Produce detailed case summaries and analyses of specific court opinions. |
| `citation-binder` | Build a verified Citation Binder (Word document) from a brief, motion, or memorandum. |
| `closing-documents` | Generate real estate closing documents for a transaction. |
| `contract-intake` | Process a real estate contract and rider upload for a new transaction. |
| `date-calendaring` | Calendar all critical dates from a real estate transaction. |
| `deep-research` | Conduct comprehensive deep legal research with extended analysis and full opinion text review. |
| `discovery` | Generate discovery documents including interrogatories, requests for production, and requests for admission. |
| `exhibit-binder` | Merge a set of exhibits (PDF, Word, images) into ONE court-ready PDF binder: caption cover page, Exhibit Index with page references, a tab page before every exhibit ("EXHIBIT A"), bookmarks, "Page X of Y" on every page and optional Bates numbers. |
| `exhibits` | Attach the exhibits referenced in a certification, affirmation, affidavit or declaration: read the document, find every "attached hereto as Exhibit A is a true copy of …" reference, match each exhibit to the right file, check that the file is what the certification says it is, and produce the certification followed by tab pages and exhibits in ONE PDF (plus one PDF per exhibit and an exhibit list). |
| `hyperlinking` | Hyperlink all legal citations in a document (.docx) — case law to the opinion on Midpage (or on Descrybe when Midpage is not connected), statutes to Midpage's own law page for the section — or, without Midpage, to the section's page on law.onecle.com for that state or the U.S. Code — and federal rules to law.cornell.edu. |
| `legal-correction` | Auto-correct a legal document based on a Citation Verification Report, then re-verify the corrected document. |
| `legal-research` | Conduct professional legal research with verified case law citations. |
| `legal-verification` | Verify legal citations, case claims, and document accuracy against real case law and produce a Citation Verification Report (a .docx that pairs each proposition in the brief with the verified language of the opinion). |
| `legal-writing` | Draft professional legal documents from uploaded research and materials. |
| `pdf-form-filler` | Intelligent PDF form filling from source documents. |
| `rider-generator` | Generate a real estate contract rider for buyer or seller representation. |
| `title-review` | Review a title binder or title commitment — requirements, exceptions, chain of title, graded RED / YELLOW / GREEN — in a Title Review Report, and (seller side) generate the closing documents from it once the missing details are collected. |
| `license-status` | Show your own LVAI Pro license: licensee, seat, plan, expiry and status. |

## Requirements

- LVAI Pro runs in Claude Desktop with Cowork on a paid Claude plan (Pro or Max; Team and Enterprise through your organization owner). The phone app and the web app cannot run the file-based commands.
- The **Legal Velocity** connector, signed in with the email on your license: Customize → Connectors (older versions: your name → Settings → Connectors) → the Discover tab → search Legal Velocity → Connect — see SETUP-INSTRUCTIONS.md
- A legal-research connector for the research, deep-research, verification, correction, binder, hyperlinking and case-summary commands (/research, /deep-research, /verify, /correct, /binder, /hyperlink, /case-summary) and for /draft when it researches: **Midpage Legal Research** *or* **Descrybe Legal Engine** (each is its own subscription; see CONNECTORS.md). The skills detect which one is connected. If you connect both Midpage and Descrybe, every research command — /research, /deep-research, /case-summary, /verify, /correct, /binder, and /draft when it researches — checks every authority, holding, quotation and treatment on both services and tells you where they disagree. Links go to Midpage (Descrybe links only if you ask).
- Google Calendar or Outlook (date calendaring)

## Manual and support

Step-by-step manual (PDF): https://lvai-license-server.legalvelocity.workers.dev/public/LVAI-Pro-Manual.pdf
admin@legalvelocity.ai · https://www.legalvelocity.ai — Proprietary, all rights reserved.
