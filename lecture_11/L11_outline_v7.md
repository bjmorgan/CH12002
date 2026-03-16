# L11: Temperature Effects on Reaction Rates — Revised Outline (v7)

## 1. Opening: Closing the Loop from L1

**Narrative move:** In L1 we posed the general question: *how do temperature and pressure affect reaction rates?* The pressure question has been thoroughly answered — pressure affects rates through concentrations, which appear in rate laws. But we have said nothing about temperature. Temperature operates through *rate constants*, which are generally temperature-dependent.

**Callback to L3:** In L3 we learnt how to extract rate constants from experimental data at a single temperature. If we repeat those measurements at several temperatures, we can map out k(T). Is there a pattern?

---

## 2. The Arrhenius Equation

**Narrative move:** Most reactions speed up with increasing temperature. Students already know this from everyday experience and from A-level chemistry, where they will have met the Arrhenius equation. But can we go beyond "reactions speed up" to quantify *how much* and understand *why*?

### 2a. The empirical equation

- Arrhenius (1889) found that for a remarkably wide range of reactions, plotting ln k vs 1/T gives a straight line:

  k = A exp(−E_a/RT)

- Students will likely recognise this from A-level — emphasise that here we are going to take it seriously as a *quantitative empirical relationship* and ask what it really tells us.
- E_a is the **activation energy** and A is the **pre-exponential factor** — for now, these are empirical parameters extracted from the data. We will develop their physical meaning shortly.
- A surprisingly robust empirical result: it works for gas-phase reactions, solution-phase reactions, enzyme kinetics, industrial catalysis — across an enormous range of chemistry.
- Note on units: R in J K⁻¹ mol⁻¹ means E_a must be in J mol⁻¹ in the equation, though activation energies are usually *quoted* in kJ mol⁻¹.

### 2b. Linearised form and Arrhenius plots

- ln k = ln A − (E_a/R)(1/T)
- Plot of ln k vs 1/T: straight line, slope = −E_a/R, intercept = ln A.
- Steeper slope → larger E_a → more sensitive to temperature.
- **Figure:** Arrhenius plot (retain existing).
- **Figure:** k vs T for different E_a values (retain existing).

### 2c. Practical tools (examinable)

- Constructing Arrhenius plots from data.
- Two-temperature formula: derive by writing the linearised equation at T₁ and T₂ and subtracting:

  ln(k₂/k₁) = (E_a/R)(1/T₁ − 1/T₂)

- Rearranging for E_a, or using in reverse to predict k at a new temperature.
- Worked example: N₂O₅ decomposition (retain existing).
- The "doubling rule": for E_a ≈ 50 kJ mol⁻¹ near room temperature, a 10 K rise roughly doubles the rate.

**Skill statement:** Use the Arrhenius equation to construct an Arrhenius plot and extract E_a and A; apply the two-temperature formula to calculate E_a from rate constants at two temperatures or to predict k at a new temperature.

---

## 3. Why Do Reactions Require Energy? The Physical Origin of Energy Barriers

**Narrative move:** The Arrhenius equation confirms what we already knew — most reactions speed up with increasing temperature. But it tells us something more specific: the dependence is exponential in 1/T, with a characteristic energy scale E_a. A linear or power-law dependence would also give "speeds up with T" — so why this particular form? Understanding this will also help us understand why the Arrhenius equation is as generally useful as it is. We start with the first question: *why do reactions require energy at all?*

### 3a. The symmetric case: H + H–H → H–H + H

- The simplest possible reaction: an atom transfer where the same bond is broken and formed.
- To get from reactants to products, the H–H bond must stretch and weaken while the new H–H bond begins to form.
- At the transition point, the central H is partially bonded to both neighbours: [H···H···H]. Two partial bonds cost more energy than one full bond.
- This intermediate configuration is higher in energy than either reactants or products → there is an energy barrier.
- The barrier is a geometric/energetic inevitability of the bond-rearrangement process.
- Introduce the **reaction coordinate** as a measure of progress from reactants to products (qualitative).
- **Figure (new):** Energy profile for H + H₂. Label reactants, transition state [H···H···H], products, barrier height. ΔE = 0 for this symmetric case.

### 3b. The general principle

- The H + H₂ case illustrates a general point: in any chemical reaction, we never instantaneously convert reactants into products. Atoms must rearrange in space — bonds break and form, and this rearrangement generally requires passing through a geometric configuration that is higher in energy than either the starting materials or the products.
- This is true for bond-breaking reactions, isomerisations, and any process involving changes in molecular geometry.
- The height of this barrier depends on the specific chemistry: which bonds are being broken and formed, and how much the old bond must weaken before the new bond begins to compensate.

**Pedagogical note:** Do not identify the barrier height with E_a yet — that connection requires the Boltzmann argument in Section 4.

---

## 4. Why an Exponential Dependence? The Boltzmann Factor

**Narrative move:** We've established that most reactions require molecules to surmount an energy barrier. But why does that produce an *exponential* dependence on 1/T? The answer lies in how energy is distributed among molecules at thermal equilibrium — something students have already met.

### 4a. The general principle

- Students have met the Boltzmann distribution in two contexts this year:
  - **Spectroscopy:** relative populations of energy levels go as exp(−ΔE/k_BT) — higher-energy states are exponentially less populated.
  - **Kinetic theory of gases:** the Maxwell–Boltzmann distribution of molecular speeds/energies.
- Cross-reference both courses explicitly.
- These are instances of a general principle: **at thermal equilibrium, the fraction of molecules with energy exceeding some threshold E is proportional to exp(−E/k_BT).**

### 4b. Illustrative example — the Maxwell–Boltzmann energy distribution

- Since students have studied kinetic theory, use the familiar distribution as a concrete illustration.
- **Figure (new):** Maxwell–Boltzmann energy distribution at two temperatures, with the region above a threshold shaded. At higher T the distribution broadens and the shaded fraction grows.
- The shaded fraction goes as exp(−E/RT).
- Note: the collision-energy case is one specific example. The principle is more general — it applies to vibrational energy (relevant to unimolecular reactions), energy along a reaction coordinate, or any other degree of freedom. The exponential dependence on energy is a universal feature of thermal equilibrium.

### 4c. Connecting barriers to the Arrhenius equation

- The rate of most reactions is proportional to: (rate of attempts) × (fraction with enough energy to surmount the barrier).
- The Boltzmann distribution tells us the second factor goes as exp(−barrier height/RT).
- So k ∝ exp(−barrier height/RT) — which is the Arrhenius form.
- **Now we can make the identification:** for a single elementary step, the Arrhenius activation energy E_a corresponds to the height of the energy barrier, and the pre-exponential factor A corresponds to the rate of attempts.
- This is not a derivation of the Arrhenius equation — it is a justification for *why* the empirical exponential form is not unreasonable, and why it works as broadly as it does. The equation was discovered empirically and its generality extends beyond cases where a simple single-barrier picture applies.

**Caveat (flagged here, developed fully in Section 7):** The identification E_a = barrier height holds for a single elementary step, or when the rate is dictated by a single rate-determining step. For multi-step mechanisms, the measured E_a is a composite quantity.

---

## 5. Forward and Reverse Reactions: E_a and Equilibrium

**Narrative move:** So far we've considered a symmetric reaction where reactants and products are identical. What happens when they are different?

### 5a. The asymmetric case: H–H + Br → H + H–Br (and the reverse)

- Different bond strengths (D(H–H) ≈ 436, D(H–Br) ≈ 366 kJ mol⁻¹) → asymmetric energy profile → different E_a in each direction.
- **Key result:** E_a,forward − E_a,reverse = ΔE. The two barrier heights are not independent — they are constrained by thermodynamics. This drops directly out of the asymmetric energy profile diagram.
- **Rule of thumb:** For similar types of reaction, more exothermic → lower forward barrier. Approximate correlation, not a law.
- **Figure (new):** Asymmetric reaction coordinate diagram. Label E_a,f, E_a,r, ΔE.

### 5b. The link to equilibrium

- Write the Arrhenius equation for both forward and reverse:

  K = k_f/k_r = (A_f/A_r) exp(−ΔE/RT)

- Forward and reverse rate constants are not independent — they must be consistent with the equilibrium constant (**principle of detailed balance**).
- This is not a new constraint — it follows directly from the energy profile.
- **Callback:** Students have seen K = k_f/k_r in earlier lectures (pre-equilibrium, L4–5). The Arrhenius picture shows *why* this works: both rate constants are determined by the same energy surface.

---

## 6. What Determines A? The Pre-Exponential Factor for Elementary Steps

**Narrative move:** Section 4 identified A as "the rate of attempts." What determines this physically?

### 6a. Bimolecular elementary steps

- A captures the rate of molecular encounters with appropriate orientation.
- Two contributions: (1) collision frequency — how often molecules meet; (2) steric/orientation factor — whether they meet in the right geometry.
- Reactions between atoms (no orientation requirement): A close to gas-kinetic collision frequency, ~10¹⁰–10¹¹ dm³ mol⁻¹ s⁻¹.
- Reactions requiring precise alignment: A orders of magnitude lower.
- The wide range of measured A values reflects the *chemistry* of the encounter.

### 6b. Unimolecular elementary steps

- A reflects the frequency at which sufficient vibrational energy accumulates in the reactive mode.
- A vibrationally excited molecule has its energy distributed across all vibrational motions — stretches, bends, internal rotations. For reaction to occur, sufficient energy must accumulate in the *specific* motion that leads to bond breaking or rearrangement.
- Characteristically of the order of a vibrational frequency (~10¹²–10¹⁴ s⁻¹), but may be lower for complex molecules with many competing modes — the energy has to find its way into the right place, not just be in the molecule.
- **Callback to Lindemann:** The whole point of collisional activation (k₁ step) is to put energy into the molecule. A* doesn't react instantly because the energy isn't necessarily in the reactive mode yet. A for the k₂ step reflects how quickly it gets there.

**Pedagogical note:** This is where the chemistry comes back in. A large floppy molecule has many vibrational modes for the energy to "hide" in. The pre-exponential factor encodes molecular structure, not just physics.

### 6c. Forward look to Y2

- Brief sentence: "Transition state theory, which you will meet in Year 2, formalises this picture — asking *what are the properties of the partially-bonded transition state*, and how do they determine both A and E_a?"

---

## 7. The Measured E_a Is Not (In General) a Single Microscopic Barrier

**Narrative move:** Sections 3–6 established the physical meaning of E_a and A *for elementary steps*. But most reactions are not single elementary steps — and the measured Arrhenius parameters are macroscopic, empirical quantities. This is why the Arrhenius equation's generality extends beyond the simple barrier picture.

### 7a. The general point

- For multi-step mechanisms, k_obs is built from combinations of elementary rate constants (pre-equilibrium, SSA, Lindemann — all seen previously). Each elementary k has its own A and E_a.
- The observed E_a is a composite — it does not correspond to any single energy barrier.
- Likewise, the observed A is a composite and does not have a simple "collision frequency" or "vibrational frequency" interpretation.
- E_a ≈ barrier height *only* when the observed rate constant corresponds to a single elementary step, or when the rate is dictated by a single rate-determining step whose barrier dominates k_obs.
- **Common mistake (even in research papers):** Directly equating a measured Arrhenius E_a with the barrier height for a single mechanistic step, without stating the assumptions under which this identification is valid.

### 7b. Azomethane / Lindemann sidebar (callback to L7)

- In L7, we said the temperature dependence of azomethane decomposition "tells us that the reacting molecules must overcome an energy barrier." That reasoning was correct — there *is* a barrier.
- But the Lindemann mechanism involves k₁, k₋₁, and k₂. At high pressure, k_obs = k₁k₂/k₋₁.
- E_a,obs = E_a,1 − E_a,−1 + E_a,2. The measured activation energy encodes information about all three steps.
- **Pedagogical note:** Intellectual honesty moment — explicit about the simplification in L7. Students now have the tools to appreciate the nuance.

**Skill statement:** Explain why the observed activation energy for a multi-step mechanism is, in general, a composite quantity that does not correspond to a single energy barrier.

---

## 8. Three Regimes of Temperature Dependence

**Narrative move:** With the elementary/composite distinction established, survey the landscape of what temperature dependence can tell us.

### 8a. Positive E_a — the common case

- Most reactions: k increases with T, negative slope on Arrhenius plot.
- Elementary steps: reflects a genuine energy barrier (Sections 3–4).
- Multi-step mechanisms: E_a,obs is composite but still positive (Section 7).
- These two cases are **indistinguishable from the Arrhenius plot alone** — mechanistic information is needed to interpret the number.

### 8b. Near-zero E_a — approximately barrierless

- Very weak temperature dependence.
- Examples: radical–radical recombinations, diffusion-controlled reactions.
- Physical picture: no significant barrier to overcome; rate limited by encounter frequency, not energy. Note that radical recombinations *are* single elementary steps — the near-zero E_a genuinely reflects the absence of a significant barrier, precisely because no bonds need to be partially broken to form the new bond.

### 8c. Negative apparent E_a — a mechanistic diagnostic

- Rate *decreases* with T. Positive slope on Arrhenius plot.
- **Callback:** NO oxidation (L7): k_obs = k₂K, where K for the exothermic pre-equilibrium decreases with T (Le Chatelier) faster than k₂ increases.
- **Key insight:** Negative E_a is impossible for a single elementary step (all microscopic barriers are ≥ 0) → its observation is direct evidence for a multi-step mechanism.
- Retain existing figure and explanation.

**Skill statement:** Explain why the NO oxidation reaction has a negative apparent activation energy, and why negative apparent E_a implies a multi-step mechanism.

---

## 9. Non-Arrhenius Behaviour: Curved Arrhenius Plots as Mechanistic Information

**Narrative move:** So far we've discussed straight Arrhenius plots (positive, near-zero, or negative slope). But some reactions give *curved* Arrhenius plots. Rather than being a nuisance, this curvature is mechanistic information.

### 9a. Competing pathways

- When two parallel pathways with different activation energies contribute to the overall rate, k_obs = k₁ + k₂.
- At low T, the low-E_a pathway dominates; at high T, the high-E_a pathway takes over.
- The Arrhenius plot shows two approximately linear regions with different slopes, connected by a curve.
- **Figure:** Curved Arrhenius from competing pathways (retain/update existing figure).

### 9b. Change of rate-limiting step

- **The example:** A → B → P (consecutive mechanism from L4–5).
- Under SSA: k_obs = k₁k₂/(k₁ + k₂).
- Limiting cases: k_obs ≈ k₁ when k₁ ≪ k₂ (step 1 is RLS); k_obs ≈ k₂ when k₂ ≪ k₁ (step 2 is RLS).
- If E_a,1 ≠ E_a,2, the slower step swaps at some crossover temperature — the step with the higher E_a "catches up" as T increases.
- **Figure (new):** Two dashed lines (ln k₁ and ln k₂, different slopes) with solid curve (ln k_obs) tracking whichever is lower. Annotate crossover and limiting slopes. Concrete numbers: e.g. E_a,1 = 30, E_a,2 = 80 kJ mol⁻¹, A values chosen for crossover ~400–500 K.

**Key insight:** In both cases, a curved Arrhenius plot is *information*, not just non-ideal behaviour. It tells you something about the mechanism — either that there are competing pathways, or that the identity of the bottleneck shifts with temperature.

---

## 10. Course Synthesis: Temperature Dependence as a Mechanistic Probe

**Narrative move:** Pull together the course-long narrative. The question from L1 is now fully answered.

- **The toolkit we've built:** experimental data → rate laws (L1–3) → mechanisms via SSA and pre-equilibrium (L4–5) → application to real systems (L7–10) → temperature dependence reveals energy barriers and tests mechanisms (L11).
- **The hierarchy of what E_a tells you:**
  - Elementary step (or single RDS): approximately the barrier height
  - Multi-step mechanism: a composite encoding multiple barriers
  - Sign and magnitude: mechanistic diagnostics
  - Curvature in the Arrhenius plot: reveals changes in rate-limiting step or competing pathways
- **The overarching course question** ("how do we extract molecular-level understanding from macroscopic measurements?") is answered: concentration dependence gives us the rate law; the rate law constrains the mechanism; temperature dependence provides independent information about energy barriers and tests mechanistic proposals.
- **Forward look:** Y2 TST connects A and E_a to molecular properties of the transition state.

---

## 11. Key Concepts

- The **Arrhenius equation**, k = A exp(−E_a/RT), is an empirical relationship that describes how rate constants depend on temperature. It is remarkably general, applying across a huge range of chemical systems.
- An **Arrhenius plot** (ln k vs 1/T) gives a straight line with slope −E_a/R and intercept ln A.
- The **two-temperature formula** allows determination of E_a from measurements at two temperatures, or prediction of k at a new temperature.
- Reactions generally require energy because bond rearrangement passes through a high-energy transition state — atoms must rearrange in space, and this generally involves moving through a geometric configuration higher in energy than either reactants or products.
- The exponential dependence on 1/T reflects the **Boltzmann distribution** — familiar from spectroscopy and kinetic theory — which tells us the fraction of molecules with energy exceeding a threshold goes as exp(−E/RT).
- For a single elementary step (or a mechanism dominated by a single RDS), E_a corresponds to the barrier height and A to the rate of attempts.
- For an asymmetric reaction, E_a,f − E_a,r = ΔE, and k_f/k_r = K — rate constants are constrained by thermodynamics (**detailed balance**).
- For a **bimolecular** elementary step, A reflects collision frequency × orientation probability. For a **unimolecular** step, A reflects the frequency at which vibrational energy accumulates in the reactive mode — lower for complex molecules with many competing vibrational modes.
- For **multi-step mechanisms**, the measured E_a and A are composites that do not correspond to single microscopic barriers or attempt frequencies. This distinction is frequently overlooked, even in research literature.
- A **negative apparent E_a** implies a multi-step mechanism. A **curved Arrhenius plot** can indicate competing pathways or a change in the rate-limiting step with temperature. Both are mechanistic diagnostics.
- Temperature dependence complements concentration dependence as a probe of reaction mechanisms.

---

## Figures

### Summary table

| # | Figure | Section | Status | Priority |
|---|--------|---------|--------|----------|
| 1 | H + H–H symmetric energy profile | 3 | **New** | Essential |
| 2 | H–H + Br asymmetric energy profile | 5 | **New** | Essential |
| 3 | Maxwell–Boltzmann energy distribution at two T | 4 | **New** | Essential |
| 4 | Three-panel Arrhenius plot summary (positive / ~zero / negative slope) | 8 | **New** | Nice-to-have |
| 5 | RLS crossover Arrhenius plot | 9b | **New** | Essential |
| 6 | Arrhenius plot (straight line) | 2 | **Exists** | Retain |
| 7 | k vs T for different E_a | 2 | **Exists** | Retain |
| 8 | Negative E_a Arrhenius plot | 8 | **Exists** | Retain (but may be superseded by #4) |
| 9 | Curved Arrhenius (competing pathways) | 9a | **Exists** | Update for visual consistency with #5 |
| 10 | Reaction coordinate (generic) | — | **Exists** | Superseded by #1 and #2 |

### Detailed figure specifications

**Figure 1: H + H–H symmetric energy profile (Section 3) — NEW, essential**

This is the key figure for "why barriers exist." Specifications:
- Energy on the y-axis, reaction coordinate on the x-axis.
- Reactants (H + H–H) and products (H–H + H) at the same energy level (ΔE = 0).
- The transition state [H···H···H] at the top of the barrier.
- Barrier height clearly labelled — but **not** labelled as E_a (that identification comes later in Section 4).
- Small molecular diagrams at three points along the coordinate showing bond lengths changing: H far from H–H → H···H···H symmetric → H–H far from H. These make the connection between "position on the reaction coordinate" and "what the atoms are actually doing" — without them it's just an abstract bump.

Consider pairing with Figure 2 as panels (a) and (b) of a single figure for immediate visual comparison.

**Figure 2: H–H + Br asymmetric energy profile (Section 5) — NEW, essential**

Specifications:
- Same format as Figure 1 but with reactants and products at different energy levels.
- E_a,f and E_a,r both labelled, with ΔE as the difference clearly indicated.
- Both directions of the reaction shown.
- Should be visually paired with Figure 1 (e.g. side-by-side panels) so students can see exactly what changes when the symmetry is broken.

**Figure 3: Maxwell–Boltzmann energy distribution at two temperatures (Section 4) — NEW, essential**

This is the "fraction of molecules with enough energy" figure. Specifications:
- Two distribution curves at clearly labelled temperatures (T₁ and T₂, with T₂ > T₁).
- A vertical line at a threshold energy.
- The area to the right of the threshold shaded for both curves — visibly larger at T₂.
- Axes: probability (or number of molecules) vs energy.
- Present this as the Maxwell–Boltzmann KE distribution students have already seen in kinetic theory — keep the shape and axes familiar. It is used as an *illustration* of the general Boltzmann principle, not as the only case.
- The threshold can be labelled as E_a at this point (Section 4 is where the identification is made).

**Figure 4: Three-panel Arrhenius plot summary (Section 8) — NEW, nice-to-have**

A compact visual summary of the three regimes of temperature dependence. Specifications:
- Three small Arrhenius plots side by side: (a) negative slope (positive E_a, normal), (b) near-zero slope (E_a ≈ 0, barrierless), (c) positive slope (negative apparent E_a).
- Each panel labelled with the regime and a brief descriptor.
- Functions as a quick-reference summary: "what does my Arrhenius plot tell me?"
- The contrast between the three panels reinforces the point that the slope is mechanistic information.

If this figure is made, the existing standalone negative E_a Arrhenius plot (Figure 8) may become redundant.

**Figure 5: RLS crossover Arrhenius plot (Section 9b) — NEW, essential**

The most novel and pedagogically interesting figure. Specifications:
- Two dashed straight lines representing ln k₁ and ln k₂ individually (different slopes reflecting E_a,1 = 30 kJ mol⁻¹ and E_a,2 = 80 kJ mol⁻¹).
- A solid curve for ln k_obs = ln(k₁k₂/(k₁ + k₂)) that follows whichever elementary k is lower at each temperature.
- The crossover point clearly marked.
- The two limiting slopes annotated (matching the slopes of the individual k lines).
- Labels in the two regimes: "step 2 is RLS" (low T) and "step 1 is RLS" (high T).
- Concrete numbers: choose A values so the crossover falls around 400–500 K (e.g. A₁ = 10⁸ s⁻¹, A₂ = 10¹⁴ s⁻¹ — work out exact values to get a visually clear crossover).
- Students should be able to *see* that k_obs tracks the slower step, and that the curvature is where they're comparable.

### Figures not recommended

**Composite E_a energy diagram (Section 7):** Considered showing a two-step energy landscape (A → intermediate → P) with two barriers to illustrate how E_a,obs is composite. Decided against — the algebraic argument (E_a,obs = E_a,1 − E_a,−1 + E_a,2) is clear enough, and a figure risks oversimplifying the energy landscape for a multi-step mechanism.

**Pre-exponential factor illustration (Section 6):** Considered schematics of favourable/unfavourable collision orientations (bimolecular) or energy redistribution among vibrational modes (unimolecular). Decided against — the argument is qualitative and verbal, and a figure would give it false precision. The words do the work here.

---

## Changes Relative to Current L11

| Current | Revised | Reason |
|---------|---------|--------|
| Opens with Boltzmann/barrier motivation | Opens with L1 callback; Arrhenius presented first as empirical relationship students recognise from A-level | Epistemologically honest; equation stands as empirical fact |
| Physical picture and equation interleaved | Arrhenius equation (empirical, Section 2) → physical picture (Sections 3–4) as justification for why the form is reasonable and broadly applicable | Avoids implying Arrhenius is derived from barrier theory |
| E_a introduced as "energy barrier" from the start | E_a introduced as empirical parameter; identified with barrier height after the barrier + Boltzmann argument (Section 4c), with immediate caveat | Identification is a *result* with stated conditions, not a definition |
| Single reaction coordinate diagram without explanation of *why* barriers exist | H + H₂ atom transfer as specific illustration, then generalised: bond rearrangement always involves passing through higher-energy geometries | Students understand the physical origin, not just the diagram |
| Equilibrium connection absent | Asymmetric barriers → E_a,f − E_a,r = ΔE → K = k_f/k_r → detailed balance | Connects kinetics to thermodynamics; callbacks to L4–5 |
| A described briefly | Separate treatment: bimolecular (collisions + orientation) and unimolecular (vibrational energy redistribution, molecular complexity) | Adds the chemistry; explains why A values vary; Lindemann callback |
| No elementary/composite distinction | Explicit section with Lindemann/azomethane sidebar; conditions stated | Addresses common misconception |
| Non-Arrhenius via competing pathways only | Both competing pathways (retained) and RLS-crossover (new) | More complete picture; RLS crossover is mechanistically richer |
| Course synthesis is one paragraph | Expanded to close L1 question and summarise course narrative | L11 as culmination, not anticlimax |
