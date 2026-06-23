<p align="center">
  <img src="assets/Anchr_logo.png" alt="Anchr" width="180">
</p>

<h1 align="center">Anchr — AI Agent Guard</h1>

<p align="center"><em>With ⚓, Drift is Okay.</em></p>

<p align="center">
  A deterministic guard that catches AI coding-agent drift, hallucinated verification,
  scope creep, and false completion — before it reaches your codebase.
</p>

<p align="center">
  <a href="https://marketplace.visualstudio.com/items?itemName=vivartan.anchr"><b>Install from the VS Code Marketplace »</b></a>
</p>

---

> This is the **public home** for Anchr — overview, issues, and docs.
> Anchr is proprietary software; its source code is not published here.
> To use it, install the extension from the Marketplace link above.

## What it is

Anchr installs a `.anchr/` protocol folder into your workspace. Your AI agent
(Claude Code, Cursor, Copilot, Codex, Cline, and others) reads the protocol, works
**one atomic step at a time**, and writes a machine-readable signal after each step.
A local VS Code daemon watches those signals and runs **deterministic checks** before
the agent is allowed to continue.

On success, the status bar stays active. On a violation, Anchr enters **HARD STOP**:
it writes a lock file, shows a notification, and blocks further progress until a human
clears the lock. The agent cannot rationalize past it.

## What it catches

A drift is caught **mechanically**, not by another model's judgment. Examples :

- **Scope creep** — the agent changed a file it never declared.
- **False completion** — "done" without a passing test run.
- **Hallucinated verification** — a cited line that doesn't contain the claim.
- **Credential exposure** — secrets leaking into a signal.
- **Self-modification** — the agent editing the protocol or config.
- **Gate skipping** — implementing before required gates pass.

These map to 12 mechanical checks plus a systemic drift-detection layer (instruction
decay, autoregressive style drift, cyclical drift, temporal-rule drift, high-impact
action gating, and signal-flood protection).

## Requirements

- **Python 3.10+** on your PATH (`python`/`py` on Windows, `python3`/`python` on macOS/Linux).
- A **Git repository** — the daemon refuses to run outside one.

## Privacy  

Anchr's standard mode runs **entirely locally** and collects **no telemetry**. The daemon,
the protocol checks, and the panel never contact a server. Outbound network calls happen
only for features you explicitly invoke (e.g. source verification) or enterprise sign-in.
No code, signal, audit finding, or workspace content is ever sent anywhere by default.

## Support

- **Bug reports & feature requests:** [open an issue](https://github.com/vivartanenterprises/Anchr/issues)
- **Security disclosures:** see [SECURITY.md](SECURITY.md)

## Legal

- [LICENSE](LICENSE) — proprietary; all rights reserved
- [Privacy Policy](PRIVACY.md)
- [Terms of Service](TERMS.md)

© 2026 Vivartan Enterprises. All rights reserved. "Anchr" and the anchor mark are
trademarks of Vivartan Enterprises.
