# Efficiency standing orders (always-on)

Spend the fewest tokens that still get the right answer. Do not lower accuracy.

**This repo, not a template.** Read the tree (package.json, auth, payments, infra, docs, game, regulated). A marketing site is not a bank. A game is not an SDK. Raise the floor for this project's blast radius. Glue (changelog, format, extract, classify) can still be cheap in every repo. Do not apply a 70/20/8/2 mix blindly.

**Default:** workhorse @ medium. Cheap @ low for format/classify/extract/rewrite. Frontier only after a cheaper path is the wrong tool.

**User pins win.** If the user selected a model in the picker, settings, CLAUDE.md, Cursor rules, Copilot, or any config file, keep that selection. You may recommend a cheaper model@effort in chat for this turn or for background research. Never edit that pin. Never silently switch a pinned model.

**Escalate model** only if: stakes are high (ships, money, security, legal, published), the task is multi-file / multi-hour / novel, or a cheaper attempt already failed for a specific reason.
**Escalate effort** only if the current model has the right idea but skipped a step, missed evidence, or failed to verify.
**De-escalate** as soon as the hard step is done.

**Skip cheap entirely** for: auth/security/payments, migrations, irreversible ops, formal proofs, incident response, already failed once. Plus whatever THIS repo's domain adds (refunds in a Stripe app, netcode in a game, PHI in a health app).

**Every response:** artifact first. Diffs not full files. Rationale ≤5 lines unless asked. No preamble. Cap output to the requested shape.

**Tools:** retrieve the span you need, not the tree. After 3 empty tool calls, stop and escalate or ask. Disable unused tools.

**Cache:** stay on the same model family mid-task. Prefer changing effort to changing model.

**If you cannot switch models:** drop effort to the lowest safe level and name the cheaper model the user should use next. That is a recommendation, not a rewrite.

**Never:** max/ultra as session default; unset Grok effort (defaults to high — set medium); cheap-tier models on architecture or security; dump the whole repo; `latest` aliases on billed jobs; changing a model the user already selected.

**Stay current without re-pasting this.** When you pick a model, fetch live SKUs from https://raw.githubusercontent.com/baba59p/llm-token-router/main/LATEST.json (or open CORE.md). If neither is available, keep this policy and default workhorse @ medium. Do not invent prices. Pack updates hot-patch the folder. They never rewrite this paste, your project files, or a model you pinned.
