# Connectors

## Required

**Legal Velocity** — delivers every skill's instructions, references, scripts and templates under your license.
Tools: `get_skill`, `get_reference`, `get_script`, `get_template`, `license_status`.
Connect it from Claude's directory: Customize → Connectors (older versions: your name → Settings → Connectors) → the Discover tab → search Legal Velocity → Connect. Not listed yet? Click + → Add custom connector, name it Legal Velocity, enter https://mcp.legalvelocity.ai/mcp, click Add, then Connect. Sign in with the email address on your license, enter the 6-digit code we email you, choose your seat and click Allow.

**One legal-research connector** — legal research, deep research, verification, correction, citation binders, hyperlinking, case summaries, and drafting when it researches. Either:

- **Midpage Legal Research** (`search`, `analyzeCaseDocument`, `analyzeCaseDocket`, `searchLaws`, `analyzeLaw`) — account at https://app.midpage.ai/sign-up; listed in Claude's connector directory as *Midpage Legal Research*: Customize → Connectors (older versions: your name → Settings → Connectors) → the Discover tab; or
- **Descrybe Legal Engine** (`search_cases_by_concept`, `find_case_from_reference`, `get_case_passages`, `verify_quote`, `check_case_status`, `search_laws_and_rules`, …) — subscription at https://descrybe.com/connect; listed in Claude's connector directory as *Descrybe Legal Engine*: Customize → Connectors (older versions: your name → Settings → Connectors) → the Discover tab.

The skills detect which one is connected. If you connect both Midpage and Descrybe, every research command — /research, /deep-research, /case-summary, /verify, /correct, /binder, and /draft when it researches — checks every authority, holding, quotation and treatment on both services and tells you where they disagree. Links go to Midpage (Descrybe links only if you ask).

## Optional

| Category | Options |
|----------|---------|
| Calendar | Google Calendar, Microsoft Outlook / Office 365 |
| Drive | Google Drive |
| Email | Gmail |
| Chat | Slack |
