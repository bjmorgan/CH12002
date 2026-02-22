# CH12002 L2–L3 Revision Brief

## File Mapping

| Old file | New lecture | New file |
|----------|-----------|----------|
| `lecture_03.Rmd` | L2: Integrated Rate Laws | `lecture_02.Rmd` |
| `lecture_04.Rmd` | L3: Determining Rate Laws | `lecture_03.Rmd` |

---

## New L2 Changes (lecture_03.Rmd → lecture_02.Rmd)

### 1. Rewrite opening paragraph
Currently references old L2 ("unimolecular decomposition reactions" lecture, now dropped). Must connect to new L1 (rates, rate laws, mass balance, elementary processes).

### 2. Add azomethane worked example (~200–300 words)
Data table and first-order confirmation currently only in lecture_04.Rmd. New L2 should introduce the dataset: show ln[azomethane] vs t plot → straight line → confirms first-order → extract k = 9.6 × 10⁻³ min⁻¹. This is the first real dataset students encounter.

**Data:**
| t / minutes | 0 | 30 | 60 | 90 | 120 | 150 | 180 |
|-------------|---|----|----|----|----|-----|-----|
| [azomethane] / 10⁻³ mol dm⁻³ | 8.70 | 6.52 | 4.89 | 3.67 | 2.75 | 2.06 | 1.55 |

### 3. Add half-life preview section (~200 words)
Currently no half-life content in L2. Derive t₁/₂ = ln 2/k for first-order, note it is constant (independent of [A]₀), briefly mention this is not true for other orders. Full diagnostic treatment deferred to L3.

### 4. Add summary table
Three integrated rate laws side-by-side (order, integrated form, linear form, plot axes, slope). Exists in slides and course design but not in notes.

### 5. Pseudo-first-order placement
Currently at end of file. Course design places full treatment in L3 (isolation method context). Options: (a) move entirely to L3, (b) keep brief mention with forward reference.

### 6. Fix author's note
Stray comment in graphical analysis section: "(note somewhere that the same process can be applied to *any* simple rate law...)" — convert to proper prose or remove.

---

## New L3 Changes (lecture_04.Rmd → lecture_03.Rmd)

### 1. Update opening paragraph
Currently: "As we saw in Lecture 3, different rate laws lead to different integrated rate laws" — update reference to new L2.

### 2. Reframe azomethane as revisit
Existing draft introduces azomethane as new. New structure: students already met data in L2 and confirmed first-order. L3 should say something like: "Returning to our azomethane data from the previous chapter, we now apply the integral method *systematically*..."

### 3. Add 2nd-order rejection plot (~100 words)
Course design is explicit: "also show that 2nd order plot is *not* linear." Plot 1/[A] vs t → curved → inconsistent with 2nd order. Exists in old L4 slides but missing from notes. Critical for showing systematic testing.

### 4. Half-life section coordination
Since L2 now previews basic t₁/₂ derivation, L3 should acknowledge this and focus on the *method*: using constant proportional change as diagnostic, generalised t₁/ₙ result, applying to azomethane data. Existing draft mostly has this but needs a connecting sentence.

### 5. Confirm pseudo-first-order placement
Should be fully treated in L3 (isolation method context), with at most brief mention in L2.

---

## Change Matrix

| Change | L2 | L3 | Effort |
|--------|----|----|--------|
| Rewrite opening paragraph | ✓ | ✓ | Small |
| Add azomethane worked example | ✓ | — | ~200–300 words |
| Add half-life preview | ✓ | — | ~200 words |
| Add summary table | ✓ | — | Small |
| Add 2nd-order rejection plot | — | ✓ | ~100 words |
| Reframe azomethane as revisit | — | ✓ | Small |
| Coordinate half-life content | — | ✓ | Small |
| Resolve pseudo-first-order placement | ✓ | ✓ | Small |
| Fix author's note | ✓ | — | Small |

---

## Key Reference Data

**Azomethane first-order analysis:**
- ln[A] vs t gives slope = −k = −9.6 × 10⁻³ min⁻¹ (= 1.6 × 10⁻⁴ s⁻¹)

**Azomethane half-life analysis:**
- Δt = 72.3 min (constant for successive halvings)
