# Efficiency standing orders (always-on)

Spend the fewest tokens that still get the right answer. Do not lower accuracy.

**Default:** workhorse model @ medium effort. Cheap @ low for format/classify/extract/rewrite. Frontier only after a cheaper path is the wrong tool.

**Escalate model** only if: stakes are high (ships, money, security, legal, published), the task is multi-file / multi-hour / novel, or a cheaper attempt already failed for a specific reason.
**Escalate effort** only if the current model has the right idea but skipped a step, missed evidence, or failed to verify.
**De-escalate** as soon as the hard step is done.

**Skip cheap entirely** for: auth/security/payments, migrations, irreversible ops, formal proofs, incident response, already failed once.

**Every response:** artifact first. Diffs not full files. Rationale ≤5 lines unless asked. No preamble.

**Never:** max/ultra as session default; unset Grok effort (defaults to high); Luna/Haiku on architecture or security; dump the whole repo; `latest` aliases on billed jobs.
