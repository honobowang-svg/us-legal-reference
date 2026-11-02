# US Legal Reference Assistant — Knowledge Base

Free, public **United States** legal **reference** knowledge base for a single Grok Bot with internal triage.

**Not legal advice. Not a lawyer.** Statutes and numbers change; always verify against official sources and consult a licensed attorney in your state.

## What this is

- **Federal baseline** plus **state-specific** notes.
- **Fully covered states (first priority):** California, Texas, New York, Florida, Illinois.
- **Other states:** federal baseline + clear warning that state-specific rules must be checked on the official state legislature / courts self-help site (links in `bot_master_prompt.md`).
- **11 branches**, each with five files: `system_prompt.md`, `knowledge_base.md`, `calculators.md`, `deadlines.md`, `templates.md`.

## Branches

| Dir | Topic |
|-----|--------|
| `family/` | Family / divorce / custody / support |
| `inheritance/` | Wills, probate, intestacy |
| `contracts/` | Contracts / consumer credit (civil) |
| `torts/` | Personal injury / torts |
| `property/` | Real property / landlord–tenant |
| `employment/` | Employment & wage / overtime |
| `criminal/` | Criminal **rights & procedure only** (no sentence prediction, no evasion help) |
| `business/` | Business entities & intellectual property |
| `admin/` | Administrative / immigration (**reference only**) |
| `consumer/` | Consumer protection & online |
| `procedure/` | Civil procedure & small claims |

## How to use (Bot assembly)

1. Paste / attach root `bot_master_prompt.md` as the Bot Instructions.
2. Attach each branch’s five files as knowledge.
3. Do **not** attach `test_cases.md` or `eval_report.md` as runtime knowledge unless you want them for QA.

## Verification rule

Quote statute text only from official sources (e.g. [uscode.house.gov](https://uscode.house.gov/), [eCFR](https://www.ecfr.gov/), official state legislature sites, courts’ self-help). Cite title/section and effective/amended date. Anything not fully verified is marked **`[TO VERIFY]`** — never invent statutes, dollar figures, or case holdings.

## Disclaimer (every answer)

This project provides **reference information only**. It is **not legal advice**, the assistant is **not a lawyer**, and users should **consult a licensed attorney in their state**.

## License / cost

Free public reference materials. No affiliation with any commercial marketplace or private company brand is implied.

