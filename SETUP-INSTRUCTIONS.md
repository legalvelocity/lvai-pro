# LVAI Pro — Setup

LVAI Pro runs in Claude Desktop with Cowork on a paid Claude plan (Pro or Max; Team and Enterprise through your organization owner). The phone app and the web app cannot run the file-based commands.

0. **Upgrading?** Remove any earlier *LVAI Pro* or *Legal Velocity* plugin first (Customize → Plugins → open the plugin → ⋮ → Remove),
   otherwise you will see every skill twice.
1. **Connect Legal Velocity.** In Claude Desktop, open:
   **Customize → Connectors (older versions: your name → Settings → Connectors) → the Discover tab → search Legal Velocity → Connect**. Not listed yet? Click + → Add custom connector, name it Legal Velocity, enter https://mcp.legalvelocity.ai/mcp, click Add, then Connect.
   Sign in with the email address on your license, enter the 6-digit code we email you, choose your seat and click Allow. Each seat works on one Claude account at a time: signing in from another account signs the first one out (you get an email). A colleague needs a seat of their own.
   *Team / Enterprise:* an organization Owner connects it under Organization settings → Connectors;
   each member then clicks **Connect** and signs in.
   *Issued a personal connector URL before October 2026?* It still works: Customize → Connectors → + → Add custom connector (older versions: your name → Settings → Connectors), name it `Legal Velocity`, paste the URL.
2. **Install this plugin.** From Claude's directory (Customize → Plugins → Discover → *LVAI Pro* → Install), or download it from
   https://lvai-license-server.legalvelocity.workers.dev/public/lvai-pro.plugin (the button in your setup email), then double-click the downloaded `lvai-pro.plugin` or drag it onto the
   Claude Desktop window (or Customize → Plugins → upload).
3. **Connect a legal-research service** — the research, deep-research, verification, correction, binder, hyperlinking and
   case-summary commands (and /draft when it researches) need one of these (your own subscription, separate from LVAI Pro):
   - **Midpage Legal Research** — sign up at https://app.midpage.ai/sign-up (two-week free trial, then per-seat plans), then in Claude:
     **Customize → Connectors (older versions: your name → Settings → Connectors) → the Discover tab** → search *Midpage* → **Connect** → sign in with your Midpage account.
   - **Descrybe Legal Engine** — subscribe at https://descrybe.com/connect (Legal Engine or Platform plan), then in Claude:
     **Customize → Connectors (older versions: your name → Settings → Connectors) → the Discover tab** → search *Descrybe* → **Connect** → sign in with your Descrybe account → allow all tools.
   One is enough; the commands detect which is connected. If you connect both Midpage and Descrybe, every research command — /research, /deep-research, /case-summary, /verify, /correct, /binder, and /draft when it researches — checks every authority, holding, quotation and treatment on both services and tells you where they disagree. Links go to Midpage (Descrybe links only if you ask).
   Also connect **Google Calendar / Outlook** (same Discover tab) for date calendaring.
4. **Verify.** Ask Claude: "Check my LVAI Pro license status." Then try any skill. If Claude says the connector isn't
   available, click **+** in the message box → **Connectors** and switch Legal Velocity on for that chat.

Step-by-step manual (PDF, with pictures): https://lvai-license-server.legalvelocity.workers.dev/public/LVAI-Pro-Manual.pdf
Renewals, extra seats and support: admin@legalvelocity.ai
