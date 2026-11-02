# US Legal Reference Assistant · Architecture (Single Bot Internal Triage)

> Workspace: `/workspace/global-law-agents/us/`  
> Free public **legal reference** knowledge base (not legal advice).  
> Assembled as **one** Grok Bot with internal routing (not multiple bots).  
> Revision: 2026-11-02 (Asia/Shanghai)

---

## 1. Design goals

1. Mirror the China pack structure (`falv-pub`): master prompt + 11 branches × 5 files.
2. **State-first triage** because US law is heavily state-based (owner requirement).
3. Federal baseline always available; **deep packs** for CA, TX, NY, FL, IL.
4. Criminal = rights/procedure only; immigration = reference only.
5. Never fabricate statutes; mark gaps **`[TO VERIFY]`**.

---

## 2. Runtime assembly

| Layer | File(s) | Role |
|-------|---------|------|
| Instructions | `bot_master_prompt.md` | Persona, triage, routing, hard refusals, disclaimer |
| Branch playbooks | `*/system_prompt.md` | Scope, refuse list, flow |
| Knowledge | `*/knowledge_base.md` | Cited statutes / official portals |
| Tools | `*/calculators.md` | Formulas (MW/OT, small claims, SOL tables) |
| Clocks | `*/deadlines.md` | Limitation / procedure clocks |
| Forms | `*/templates.md` | Checklists / letter skeletons |
| QA (optional) | `test_cases.md`, `eval_report.md` | Do **not** attach as user-facing knowledge unless testing |

---

## 3. Triage sequence

```
User question
  → Ask STATE (and federal vs state) if missing
  → Route to one of 11 categories
  → Load that branch five-pack
  → Answer with citations + disclaimer
```

If multi-issue (e.g., wage claim + small claims filing): primary branch first; cross-link `procedure/` for forum/SOL.

---

## 4. State coverage policy

| Tier | States | Content |
|------|--------|---------|
| Full-first | CA, TX, NY, FL, IL | Verified quotes where fetched; calculators; SOL snapshots |
| Baseline | All others | Federal + “check state legislature” + link pattern from master prompt |

---

## 5. Safety rails

- No sentence prediction / crime-evasion / evidence destruction.
- No guaranteed visa outcomes.
- No fake statute numbers.
- Every answer ends with disclaimer (§7 of master prompt).

---

## 6. Maintenance

When a statute amends: update the branch `knowledge_base.md` quote + date line; bump any calculator table; add a regression case to `test_cases.md`.
