# EFF Pack

Stop paying frontier prices for work a cheap model can finish.

This public repo is the **free standing orders** plus a buy link.
The paid zip adds the routing table, local router, adapters, and the accuracy floor.

**Buy ($29 one-time):** https://whop.com/effpack/eff-pack

---

## If you only do one thing

Copy [`SNIPPET.md`](./SNIPPET.md) into custom instructions / Cursor user rules / Gemini system instruction.

That is the always-on text. It tells the model:

- default to a mid model, not the most expensive one
- use a cheap model for format / extract / rewrite
- skip cheap on auth, payments, incidents, and anything that already failed
- keep answers short

Do not paste a long policy into those fields. Long standing text costs more than it saves.

---

## What the paid zip adds

After you buy, open **1. DOWNLOAD THE ZIP** on Whop and download the attachment.

| In the zip | What you do with it |
|---|---|
| `START_HERE.md` | Four-minute setup |
| `CORE.md` | Keep as a **file**. Do not paste it into custom instructions |
| `bin/eff.py` | `python bin/eff.py route "your task"` — no API key |
| `DO_NOT_DEGRADE.md` | The accuracy floor |
| `adapters/` | Append onto Claude / Cursor / ChatGPT / Gemini / Grok / Copilot |
| `STATS.md` | Where the $180 vs $21.60 numbers come from |

Proof after unzip:

```bash
python bin/eff.py route "write the changelog"
# cheap @ low

python bin/eff.py route "fix the oauth refresh race in production"
# frontier @ high, skip cheap
```

---

## Catalog math (not a promise about your bill)

Fixed shape: 8,000 input + 2,000 output. 7 September 2026 list prices.

| Mix | 1,000 calls |
|---|---|
| All Fable 5.1 | $180 |
| All Terra | $40 |
| Target 70 / 20 / 8 / 2 | $21.60 |

Independent systems doing this job (not this zip): RouteLLM 85% cheaper on MT-Bench at 95% GPT-4 quality. A LiteLLM partner saved $12,249 (51%) on 273k requests vs all-flagship.

---

## Refund

If the zip will not open or `python bin/eff.py` will not run on Python 3.9+, the $29 comes back.
