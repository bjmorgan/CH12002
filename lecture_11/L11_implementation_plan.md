# L11 Implementation Plan

## Goal

Write `lecture_11/lecture_11.Rmd` from scratch, following `L11_outline_v8.md`. The existing Rmd is superseded — the structure has changed substantially.

## Source documents

| Document | Path | Purpose |
|---|---|---|
| Outline (v8) | `lecture_11/L11_outline_v8.md` | Primary spec — section content, narrative logic, figure specs, pitfalls |
| Style guide | `CH12002_lecture_notes_style_guide.md` | Voice, formatting, LaTeX conventions, checklist |
| Course design | `CH12002_course_design_2026.md` | Learning objectives (note: L12 is now a problem session) |
| Existing Rmd | `lecture_11/lecture_11.Rmd` | Source for N₂O₅ worked example, existing figure references, NO oxidation passage |
| Voice reference: L1 | `lecture_1/lecture_01.Rmd` | Sets the initial voice for the course |
| Voice reference: L7 | `lecture_7/lecture_07.Rmd` | Most recently tuned; similar territory (physical picture behind maths) |

## Voice calibration

Before writing, read the opening paragraph and one representative section from L1 and L7 to internalise the voice. L7 is the closest reference — it covers physical argumentation (Lindemann mechanism, why collisions matter) in the same register needed for L11's barrier/Boltzmann sections.

Sub-agent review passes should include "voice consistency with L1/L7" as an explicit check: read a section of L7 alongside the new L11 prose and flag any drift in register, sentence structure, or tone.

## Workflow

### Phase 0: Voice calibration

Read opening + one section each from L1 and L7. No output — this is for internalising voice before writing begins.

### Phase 1: Establish voice and notation (Sections 1–2)

**Write in main context:**
- Section 1 (Opening): ~1 page. L1/L3 callbacks. Sets tone.
- Section 2 (Arrhenius equation): ~3 pages. Empirical equation (2a), linearised form (2b), practical tools + worked example (2c).
- Lift N₂O₅ worked example from existing Rmd.
- Establish equation labels: `eq:arrhenius`, `eq:arrhenius-linear`, `eq:two-temperature`.

**Sub-agent review:** Check Sections 1–2 against outline + style guide + voice consistency with L7. Fix before proceeding.

**In parallel (sub-agent):** Generate Figure 5 Python script (RLS crossover). This is independent of the prose and computationally self-contained. Also stub Figure 3 (M–B distribution) and Figure 4 (three-panel summary) if time allows.

### Phase 2: Physical picture (Sections 3–4)

**Write in main context:**
- Section 3 (Energy barriers): ~2 pages. Naive expectation → H + H₂ → general principle.
- Section 4 (Boltzmann factor): ~2 pages. General principle (4a) → M–B illustration (4b) → connection to Arrhenius (4c).
- Key transition: Figure 3 placed in 4b with generic threshold label; E_a identification in 4c text.

**Sub-agent review:** Check Sections 3–4 against outline + style guide.

### Phase 3: Consequences and applications (Sections 5–9 + Key Concepts)

**Write in main context:**
- Sections 5–6 (Forward/reverse + pre-exponential): ~3 pages total. Establish `eq:barrier-constraint`.
- Sections 7–8 (Composite E_a + three regimes): ~3 pages. Establish `eq:ea-composite`. Adapt NO oxidation passage from existing Rmd.
- Section 9 (Non-Arrhenius + closing): ~2 pages. Biexponential treatment, closing paragraphs.
- Key Concepts: 8 bullets.

**No per-section review** — review the full draft at the end to check flow across sections.

### Phase 4: Full review and iteration

**Sub-agent:** Run /review-lecture on complete Rmd.
- Fix issues directly.
- Re-run /review-lecture if substantial changes were made.

## Figures

### Figure assignments

| # | Figure | Method | Output filename | Status |
|---|--------|--------|-----------------|--------|
| 1 | H + H–H symmetric energy profile | **Hand-drawn** (Ben) | `symmetric_energy_profile.png` | TODO — spec in outline |
| 2 | H–H + Br asymmetric energy profile | **Hand-drawn** (Ben) | `asymmetric_energy_profile.png` | TODO — spec in outline |
| 3 | Maxwell–Boltzmann at two T | **Python** | `maxwell_boltzmann_threshold.png` | TODO |
| 4 | Three-panel Arrhenius summary | **Python** | `three_regime_arrhenius.png` | TODO (nice-to-have) |
| 5 | RLS crossover Arrhenius | **Python** (numerical sim) | `rls_crossover_arrhenius.png` | TODO |
| 6 | Arrhenius plot (straight line) | **Exists** | `arrhenius_plot.png` | Retain |
| 7 | k vs T for different E_a | **Exists** | `arrhenius_k_vs_T.png` | Retain |
| 8 | Negative E_a Arrhenius plot | **Exists** | `negative_ea.png` | Retain (may be superseded by #4) |
| 9 | Curved Arrhenius (competing pathways) | **Exists** / update in Python | `curved_arrhenius.png` | Retain or update |
| 10 | Reaction coordinate (generic) | **Exists** | `reaction_coordinate.png` | Superseded by #1/#2; do not reference |

### Python scripts

Location: `/Users/benmorgan/Documents/Work/Teaching/CH12002 kinetics/Python/`
Output: `/Users/benmorgan/Documents/Work/Teaching/CH12002 kinetics/Lecture Notes/lecture_11/figures/`

Scripts to create:
- `lecture_11_figures.py` — generates Figures 3, 4 (if made), and 5.

Figure 5 procedure (from outline):
1. Arrhenius parameters: E_a,1 = 30 kJ/mol, E_a,2 = 80 kJ/mol, A₁ = 10⁸ s⁻¹, A₂ = 10¹⁴ s⁻¹. Crossover T* ≈ 435 K.
2. For each T in 300–600 K: compute k₁(T), k₂(T); generate exact [P]_t; fit pseudo-first-order to long-time portion; extract k_obs.
3. Plot ln k_obs vs 1/T (solid) with ln k₁, ln k₂ (dashed).

### Hand-drawn figures (for Ben)

**Figure 1 (symmetric energy profile):**
- Energy vs reaction coordinate
- Reactants (H + H–H) and products (H–H + H) at same level (ΔE = 0)
- Transition state [H···H···H] at top
- Barrier height labelled (NOT as E_a)
- Small molecular diagrams at three points along coordinate
- Pair as panel (a) with Figure 2

**Figure 2 (asymmetric energy profile):**
- Same format, reactants and products at different levels
- E_a,f and E_a,r labelled, ΔE indicated
- Pair as panel (b) with Figure 1

## Notation/cross-reference registry

Maintain during writing; discard after final review.

### Equation labels
| Label | Equation | Section | Status |
|---|---|---|---|
| `eq:arrhenius` | k = A exp(−E_a/RT) | 2a | |
| `eq:arrhenius-linear` | ln k = ln A − (E_a/R)(1/T) | 2b | |
| `eq:two-temperature` | ln(k₂/k₁) = (E_a/R)(1/T₁ − 1/T₂) | 2c | |
| `eq:barrier-constraint` | E_a,f − E_a,r = ΔE | 5a | |
| `eq:ea-composite` | E_a,obs = E_a,1 + E_a,2 − E_a,−1 | 7b | |

### Section anchors
| Anchor | Section | Status |
|---|---|---|
| `#sec:arrhenius` | 2 (The Arrhenius Equation) | |
| `#sec:arrhenius-linear` | 2b (Linearised form) | |
| `#sec:barriers` | 3 (Energy barriers) | |
| `#sec:boltzmann` | 4 (Boltzmann factor) | |
| `#sec:forward-reverse` | 5 (Forward/reverse) | |
| `#sec:pre-exponential` | 6 (Pre-exponential factor) | |
| `#sec:composite-ea` | 7 (Composite E_a) | |
| `#sec:three-regimes` | 8 (Three regimes) | |
| `#sec:non-arrhenius` | 9 (Non-Arrhenius) | |

### Figure labels
| Label | Figure | Section | Status |
|---|---|---|---|
| `fig:energy-profile` | Symmetric + asymmetric panels | 3a, 5a | |
| `fig:mb-distribution` | M–B at two T | 4b | |
| `fig:arrhenius-k-vs-T` | k vs T | 2 | Exists |
| `fig:arrhenius-plot` | ln k vs 1/T | 2 | Exists |
| `fig:negative-ea` | Negative E_a plot | 8c | Exists |
| `fig:curved-arrhenius` | Competing pathways | 9a | Exists |
| `fig:rls-crossover` | RLS crossover | 9b | |
| `fig:three-regime-summary` | Three-panel summary | 8 | Nice-to-have |

### Callbacks made
| From | To | Content | Status |
|---|---|---|---|
| Section 1 | L1 | Temperature question posed | |
| Section 1 | L3 | Extracting k at single T | |
| Section 4a | Spectroscopy course | Boltzmann populations | |
| Section 4a | Kinetic theory course | M–B distribution | |
| Section 5b | L4–5 | K = k_f/k_r in pre-equilibrium | |
| Section 6b | L7 | Lindemann k₂ step | |
| Section 7b | L7 | Azomethane / Lindemann | |
| Section 8c | L7 | NO oxidation | |
| Section 9b | L4 | Consecutive reaction [P]_t | |
| Section 9 closing | L1 | Temperature question answered | |

### Skill statements
| Section | Content | Status |
|---|---|---|
| 2c | Arrhenius plot, two-temperature formula | |
| 7 | Composite E_a explanation | |
| 8c | Negative E_a, NO oxidation | |

## Key decisions

- **Start fresh** — do not edit existing Rmd. Retain worked example and NO oxidation passage by lifting.
- **Voice established in Sections 1–2** — all subsequent sections inherit.
- **Sub-agents for review only** — prose written in main context for voice consistency.
- **Sub-agent for Python figures** — runs in parallel with Phase 2 prose writing.
- **Figures 1 and 2 are hand-drawn by Ben** — Rmd includes placeholder `knitr::include_graphics` calls with TODO notes.
- **L12 is a problem session** — L11 closing is the last new conceptual content.
