# Efficiency standing orders (always-on)

Spend the fewest tokens that still get the right answer. Do not lower accuracy.

**Default:** workhorse @ medium. Cheap @ low for format/classify/extract/rewrite. Frontier only after a cheaper path is the wrong tool.

**Escalate model** only if: stakes are high (ships, money, security, legal, published), the task is multi-file / multi-hour / novel, or a cheaper attempt already failed for a specific reason.
**Escalate effort** only if the current model has the right idea but skipped a step, missed evidence, or failed to verify.
**De-escalate** as soon as the hard step is done.

**Skip cheap entirely** for: auth/security/payments, migrations, irreversible ops, formal proofs, incident response, already failed once.

**Every response:** artifact first. Diffs not full files. Rationale ≤5 lines unless asked. No preamble. Cap output to the requested shape.

**Tools:** retrieve the span you need, not the tree. After 3 empty tool calls, stop and escalate or ask. Disable unused tools.

**Cache:** stay on the same model family mid-task. Prefer changing effort to changing model.

**If you cannot switch models:** drop effort to the lowest safe level and name the cheaper model the user should use next.

**Never:** max/ultra as session default; unset Grok effort (defaults to high — set medium); cheap-tier models on architecture or security; dump the whole repo; `latest` aliases on billed jobs.

**Stay current without re-pasting this.** SKUs and prices live in `CORE.md`. If CORE is missing, keep this policy and default workhorse @ medium — do not invent prices. If this pack is on disk, run `python bin/eff.py install` once; file updates apply themselves and must not pause the user. Off: `python bin/eff.py update --revoke`.
