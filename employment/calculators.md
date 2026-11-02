# Employment & Wage · Calculators

> Formulas for **reference**. Show assumptions. Local ordinances may exceed state MW.

---

## 1. Applicable minimum wage

**Rule:** `pay_rate >= max(federal_MW, state_MW, local_MW)` for covered work.

**Federal:** $7.25/hr (29 U.S.C. § 206; DOL).

**Snapshot (DOL table eff. July 1, 2026):** CA 16.90 · TX 7.25 · NY 17.00/16.00 · FL 14.00 · IL 15.00.

### Example A (CA)

- Worker in Los Angeles County, no higher local rate assumed, 2026 after Jan 1.  
- Hours: 30.  
- Floor = **$16.90 × 30 = $507.00** before overtime considerations.

### Example B (TX FLSA-covered)

- Hours: 30 non-overtime.  
- Floor = **$7.25 × 30 = $217.50**.

---

## 2. Federal overtime (weekly)

**For covered nonexempt under FLSA:**

Let `H` = hours worked in the workweek; `R` = regular rate.

If `H > 40`:  
`OT_pay = (H - 40) × 1.5 × R`  
`straight_time_pay` depends on pay plan; total weekly pay must satisfy FLSA.

### Example C

- R = $20/hr; H = 50.  
- OT hours = 10.  
- OT premium pay component at 1.5×: `10 × 30 = $300` if computing 1.5× on all OT hours as total OT compensation of $300 above...  
- Clearer: OT compensation for 10 hours = `10 × 20 × 1.5 = $300`; straight 40 × 20 = $800; **total = $1,100**.

---

## 3. California daily overtime (simplified teaching model)

**Assumptions:** nonexempt; Lab. Code § 510 / Wage Order apply; no alternative workweek.

For a single workday with hours `D`:

| Band | Multiplier |
|------|------------|
| Hours ≤ 8 | 1.0× |
| Hours > 8 and ≤ 12 | 1.5× |
| Hours > 12 | 2.0× |

Plus weekly rules and seventh-day rules — run both day and week tests; **do not undercount**.

### Example D

- R = $20; one day 13 hours; other days within 8 and weekly ≤ 40 ignoring seventh-day issues.  
- Pay that day ≈ `8×20 + 4×30 + 1×40 = 160 + 120 + 40 = $320`.

---

## 4. Unpaid wage shortfall

`shortfall = (required_rate × hours) - amounts_paid` (+ OT differentials separately).

Liquidated damages / waiting-time penalties are **state-specific** (e.g., CA waiting-time penalties Lab. Code § 203) — **[TO VERIFY]** amounts before quoting.

---

## 5. FMLA eligibility checklist (not a calculator of damages)

Eligible employee generally needs: covered employer (usually 50+ employees within 75 miles — confirm statute/regs), 12 months employment, 1,250 hours worked in prior 12 months, qualifying reason. Cite 29 U.S.C. ch. 28 / 29 C.F.R. Part 825; **[TO VERIFY]** edge cases.
