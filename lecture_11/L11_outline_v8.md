# L11: Temperature Effects on Reaction Rates — Outline (v8)

This outline is a planning document for implementation of the L11 lecture notes. It specifies the structure, content, narrative logic, and figures in sufficient detail to write the Rmd directly. Annotations in **bold** are authorial notes (voice, pedagogical intent, known pitfalls) and should not appear in the final prose.

---

## 1. Opening

**Intent:** Connect to L1 and L3; establish the question this lecture answers.

In L1 we asked how temperature and pressure affect reaction rates. The pressure question has been answered throughout the course: pressure affects rates through concentrations, which appear in rate laws. Temperature is different — it operates through the rate constants themselves, which we have so far treated as fixed numbers. In L3 we learnt how to extract rate constants from experimental data at a single temperature. If we repeat those measurements at several temperatures, we can map out how k depends on T. The pattern turns out to be remarkably consistent.

**Pitfall for prose:** Frame this as a scientific observation, not a course-logistics recap. The point is that k(T) is the last piece of the puzzle, not that "we haven't covered this yet."

---

## 2. The Arrhenius Equation

**Intent:** Present the Arrhenius equation as an empirical fact that students already recognise, then develop its practical use. E_a and A are empirical parameters at this stage — their physical interpretation comes in Sections 3–6.

### 2a. The empirical equation

- Arrhenius (1889): for a remarkably wide range of reactions, plotting ln k vs 1/T gives a straight line:

  k = A exp(−E_a/RT)

- Students will recognise this from A-level. Here we take it seriously as a quantitative empirical relationship and ask what it really tells us.
- E_a and A are empirical parameters extracted from the data. E_a is traditionally called the **activation energy** and A the **pre-exponential factor** — names that anticipate a physical picture we develop in Sections 3–4.

  **Pitfall for prose:** Using the name "activation energy" here carries physical connotations before the physical picture is in place. Acknowledge this explicitly: the name is conventional; its justification comes shortly.

- A remarkably general empirical result: gas-phase reactions, solution-phase reactions, enzyme kinetics, industrial catalysis.
- Note on units: R in J K⁻¹ mol⁻¹ means E_a must be in J mol⁻¹ in the equation, though activation energies are usually *quoted* in kJ mol⁻¹.

### 2b. Linearised form and Arrhenius plots

- ln k = ln A − (E_a/R)(1/T)
- Plot of ln k vs 1/T: straight line, slope = −E_a/R, intercept = ln A.
- Steeper slope → larger E_a → more sensitive to temperature.
- **Figure (exists):** Arrhenius plot — retain.
- **Figure (exists):** k vs T for different E_a values — retain.

### 2c. Practical tools (examinable)

- Constructing Arrhenius plots from data.
- Two-temperature formula: derive by writing the linearised equation at T₁ and T₂ and subtracting:

  ln(k₂/k₁) = (E_a/R)(1/T₁ − 1/T₂)

- Rearranging for E_a, or using in reverse to predict k at a new temperature.
- Worked example: N₂O₅ decomposition — retain existing.
- The "doubling rule": for E_a ≈ 50 kJ mol⁻¹ near room temperature, a 10 K rise roughly doubles the rate.

::: {.skill}
**You should be able to:** Use the Arrhenius equation to construct an Arrhenius plot and extract E_a and A; apply the two-temperature formula to calculate E_a from rate constants at two temperatures or to predict k at a new temperature.
:::

---

## 3. Why Do Reactions Require Energy? The Physical Origin of Energy Barriers

**Intent:** Answer the question "why do reactions need energy at all?" with a concrete physical example before generalising. This section establishes that energy barriers exist; Section 4 explains why barriers produce an exponential temperature dependence.

**Naive expectation to state explicitly:** If products are lower in energy than reactants, why don't molecules simply convert? The answer is that atoms must physically rearrange — bonds break and form — and this rearrangement passes through a higher-energy configuration.

### 3a. The symmetric case: H + H–H → H–H + H

- The simplest possible reaction: an atom transfer where the same bond is broken and formed.
- To get from reactants to products, the H–H bond must stretch and weaken while the new H–H bond begins to form.
- At the **transition state**, the central H is partially bonded to both neighbours: [H···H···H]. Two partial bonds cost more energy than one full bond.
- This configuration is higher in energy than either reactants or products — there is an energy barrier.
- The barrier is a consequence of the bond-rearrangement process: you cannot get from the old bonding arrangement to the new one without passing through a geometry where neither bond is fully formed.
- Introduce the **reaction coordinate** as a measure of progress from reactants to products (qualitative — not a single geometric parameter, but a useful abstraction).

**Terminology note:** Use "transition state" consistently throughout the outline for the high-energy configuration at the top of the barrier. Define it here on first use. Do not vary between "transition point," "intermediate configuration," etc.

- **Figure 1 (new, essential):** Energy profile for H + H₂. See detailed spec in Figures section.

### 3b. The general principle

- For reactions that involve breaking and forming covalent bonds — which includes nearly all the reactions we have studied — there is generally an energy barrier. Atoms must rearrange in space, and this rearrangement passes through a geometric configuration that is higher in energy than either the starting materials or the products.
- The height of this barrier depends on the specific chemistry: which bonds are being broken and formed, and how much the old bond must weaken before the new bond begins to compensate.

**Pedagogical note:** Do not identify the barrier height with E_a yet — that connection requires the Boltzmann argument in Section 4.

---

## 4. Why an Exponential Dependence? The Boltzmann Factor

**Intent:** Explain why energy barriers produce an *exponential* dependence on 1/T. The argument is: (1) energy distributions involve Boltzmann factors (a general principle students have already met); (2) the Maxwell–Boltzmann distribution provides a concrete, familiar illustration; (3) therefore it is not surprising that the Arrhenius equation — which has a Boltzmann-like form — fits experimental data so broadly. This is a justification, not a derivation.

### 4a. The Boltzmann distribution as a general principle

- Students have met the Boltzmann distribution in two other courses this year:
  - **Spectroscopy:** relative populations of energy levels go as exp(−ΔE/k_BT).
  - **Kinetic theory of gases:** the Maxwell–Boltzmann distribution of molecular speeds/energies.
- Cross-reference both courses explicitly.
- These are instances of a general principle: **at thermal equilibrium, the probability of a molecule having energy in a particular state is proportional to exp(−E/k_BT).** This means that higher-energy states are exponentially less populated, and the fraction of molecules exceeding any energy threshold is dominated by an exponential factor.

**Note on R vs k_B:** The Boltzmann factor can be written exp(−E/k_BT) per molecule or exp(−E/RT) per mole, where E is in the corresponding units (J vs J mol⁻¹). Both forms appear in this lecture — k_BT when discussing the general Boltzmann principle; RT in the Arrhenius equation. Make the conversion explicit in the prose.

### 4b. Illustrative example: the Maxwell–Boltzmann energy distribution

- Since students have studied kinetic theory, use the Maxwell–Boltzmann KE distribution as a concrete, familiar illustration.
- **Figure 3 (new, essential):** Maxwell–Boltzmann energy distribution at two temperatures, with the region above a threshold energy shaded. At higher T the distribution broadens and the shaded fraction grows. See detailed spec in Figures section.
- The shaded area — the fraction of molecules with energy above the threshold — is dominated by a factor of exp(−E_a/RT).
- This is one specific illustration of the general Boltzmann principle. The exponential dependence on energy is not specific to translational motion — it is a universal feature of thermal equilibrium, applying equally to vibrational energy (relevant to unimolecular reactions), energy along a reaction coordinate, or any other degree of freedom.

**Pitfall for prose:** Be specific about what the figure shows (the distribution of translational KE for gas molecules, as seen in kinetic theory). Then explicitly step back to the general point. This prevents students from thinking the argument only works for gas-phase bimolecular collisions.

### 4c. Connecting barriers to the Arrhenius equation

- If a reaction requires molecules to exceed an energy threshold, and the fraction doing so goes as exp(−E/RT), then the rate constant should contain a factor of exp(−E/RT). Any remaining factors (how often molecules attempt to react, whether they are oriented correctly) are collected into the pre-exponential factor A.
- This is the simplest version of the argument: rate ∝ (rate of attempts) × (fraction with enough energy). It assumes that the dominant temperature dependence comes from the energy requirement, and that the attempt frequency is at most weakly temperature-dependent. These are reasonable assumptions for most reactions, though they are assumptions.
- **Now we can make the identification:** for a single elementary step, the Arrhenius activation energy E_a corresponds to the height of the energy barrier, and the pre-exponential factor A captures the rate of attempts (collision frequency, orientation requirements, etc.).
- This is not a derivation of the Arrhenius equation from first principles. It is a justification for why the empirical exponential form is physically reasonable, and why it works as broadly as it does. The equation was discovered empirically and its generality extends beyond cases where a simple single-barrier picture applies.

**Caveat (flagged here, developed fully in Section 7):** The identification E_a ≈ barrier height holds for a single elementary step, or when the rate is dictated by a single rate-determining step. For multi-step mechanisms, the measured E_a is a composite quantity.

---

## 5. Forward and Reverse Reactions: E_a and Equilibrium

**Intent:** Extend the barrier picture from the symmetric case (Section 3) to asymmetric reactions. Establish E_a,f − E_a,r = ΔE and the connection to detailed balance. This section can be kept brief — the key results are the figure and two equations.

### 5a. The asymmetric case: H–H + Br → H + H–Br

- Different bond strengths (D(H–H) ≈ 436, D(H–Br) ≈ 366 kJ mol⁻¹) → asymmetric energy profile → different E_a in each direction.
- **Key result:** E_a,forward − E_a,reverse = ΔE. The two barrier heights are not independent — they are constrained by thermodynamics. This drops directly out of the asymmetric energy profile diagram.
- For reactions within a similar family, more exothermic reactions tend to have lower forward barriers (Evans–Polanyi correlation). This is an approximate correlation, not a law.
- **Figure 2 (new, essential):** Asymmetric reaction coordinate diagram. See detailed spec in Figures section. Pair with Figure 1 as panels (a) and (b) of a single figure.

### 5b. The link to equilibrium

- Write the Arrhenius equation for both forward and reverse:

  K = k_f/k_r = (A_f/A_r) exp(−ΔE/RT)

- Forward and reverse rate constants are not independent — they must be consistent with the equilibrium constant (**principle of detailed balance**). The energy profile automatically ensures this consistency.
- **Callback to L4–5:** Students have seen K = k_f/k_r in the pre-equilibrium approximation. The Arrhenius picture shows *why* this relationship holds: both rate constants are determined by the same energy surface.

**Note for prose:** This is an energy-only picture (no entropy contribution). For a Y1 course this simplification is appropriate, but note briefly that a more complete treatment uses ΔG° rather than ΔE. Students who have seen K = exp(−ΔG°/RT) in thermodynamics should not be confused by the apparent inconsistency.

---

## 6. What Determines A? The Pre-Exponential Factor for Elementary Steps

**Intent:** Give physical content to A for elementary steps. This is where the chemistry comes back in — A encodes molecular structure and encounter dynamics, not just physics.

### 6a. Bimolecular elementary steps

- A captures the rate of molecular encounters with appropriate orientation.
- Two contributions: (1) collision frequency — how often molecules meet; (2) steric/orientation factor — whether they meet in the right geometry.
- Reactions between atoms (no orientation requirement): A close to gas-kinetic collision frequency, ~10¹⁰–10¹¹ dm³ mol⁻¹ s⁻¹.
- Reactions requiring precise alignment: A orders of magnitude lower.
- The wide range of measured A values reflects the chemistry of the encounter.

### 6b. Unimolecular elementary steps

- A reflects the rate at which vibrational energy accumulates in the reactive mode.
- A vibrationally excited molecule has its energy distributed across all vibrational motions — stretches, bends, internal rotations. For reaction to occur, sufficient energy must accumulate in the *specific* motion that leads to bond breaking or rearrangement.
- The timescale of vibrational motion is ~10¹²–10¹⁴ s⁻¹, which sets the upper bound for A. For complex molecules with many vibrational modes, A may be significantly lower because the energy has many places to "hide."
- **Callback to Lindemann (L7):** The whole point of collisional activation (k₁ step) is to put energy into the molecule. A* doesn't react instantly because the energy isn't necessarily in the reactive mode yet. A for the k₂ step reflects the rate of energy redistribution into the reactive mode.

### 6c. Forward look

- One sentence: "Transition state theory, which you will meet in Year 2, formalises this picture by asking what are the properties of the transition state, and how do they determine both A and E_a."

---

## 7. The Measured E_a Is Not (In General) a Single Microscopic Barrier

**Intent:** This is the most important conceptual section after the Arrhenius equation itself. Sections 3–6 built the physical picture for elementary steps. Most reactions are not single elementary steps — the measured Arrhenius parameters are macroscopic, empirical quantities. The elementary/composite distinction must be made explicit.

### 7a. The general point

- For multi-step mechanisms, k_obs is built from combinations of elementary rate constants (pre-equilibrium, SSA, Lindemann — all seen previously). Each elementary k has its own A and E_a.
- The observed E_a is a composite — it does not correspond to any single energy barrier.
- Likewise, the observed A is a composite and does not have a simple "collision frequency" or "vibrational frequency" interpretation.
- E_a ≈ barrier height *only* when the observed rate constant corresponds to a single elementary step, or when the rate is dictated by a single rate-determining step whose barrier dominates.
- **Common mistake:** Directly equating a measured E_a with the barrier height for a single mechanistic step, without stating the assumptions. If you measure E_a = 120 kJ mol⁻¹ for a multi-step reaction and equate it to a single barrier, you may significantly over- or underestimate the barrier for the actual rate-determining step.

### 7b. Worked example: azomethane / Lindemann (callback to L7)

- In L7, we said the temperature dependence of azomethane decomposition "tells us that the reacting molecules must overcome an energy barrier." That reasoning was correct — there *is* a barrier.
- But the Lindemann mechanism involves k₁, k₋₁, and k₂. At high pressure, k_obs = k₁k₂/k₋₁.
- Show the key step: take d(ln k_obs)/d(1/T) with k_obs = k₁k₂/k₋₁. Since ln k_obs = ln k₁ + ln k₂ − ln k₋₁, each term contributes its own E_a/R:

  E_a,obs = E_a,1 + E_a,2 − E_a,−1

- The measured activation energy encodes information about all three elementary steps.

**Pedagogical note:** This is an intellectual honesty moment — being explicit about a simplification made in L7 that students now have the tools to appreciate.

::: {.skill}
**You should be able to:** Explain why the observed activation energy for a multi-step mechanism is, in general, a composite quantity that does not correspond to a single energy barrier.
:::

---

## 8. Three Regimes of Temperature Dependence

**Intent:** Survey the landscape. With the elementary/composite distinction in hand, classify what different Arrhenius plots tell us.

### 8a. Positive E_a — the common case

- Most reactions: k increases with T, negative slope on Arrhenius plot.
- Elementary steps: reflects a genuine energy barrier (Sections 3–4).
- Multi-step mechanisms: E_a,obs is composite but still positive (Section 7).
- These two cases are **indistinguishable from the Arrhenius plot alone** — mechanistic information is needed to interpret the number.

### 8b. Near-zero E_a — approximately barrierless reactions

- Very weak temperature dependence.
- Examples: radical–radical recombinations, diffusion-controlled reactions.
- Physical picture: no significant energy barrier to overcome; rate limited by encounter frequency, not energy. Radical recombinations *are* single elementary steps — the near-zero E_a genuinely reflects the near-absence of a barrier, because no bonds need to be partially broken to form the new bond (contrast with Section 3's explanation of why barriers exist for bond-rearrangement reactions).

### 8c. Negative apparent E_a — a mechanistic diagnostic

- Rate *decreases* with increasing T. Positive slope on Arrhenius plot.
- **Callback to L7:** NO oxidation. k_obs = k₂K, where K is the equilibrium constant for the exothermic pre-equilibrium step. K decreases with increasing T (Le Chatelier) faster than k₂ increases → k_obs decreases overall.
- **Why negative E_a is impossible for a single elementary step:** The barrier is the energy of the transition state minus the energy of the reactants. If the transition state were lower in energy than the reactants, there would be no barrier — reactants would convert spontaneously. All microscopic barriers are ≥ 0, so all elementary E_a values are ≥ 0.
- **Key insight:** Observation of a negative apparent E_a is therefore direct evidence for a multi-step mechanism.
- **Figure (exists):** Negative E_a Arrhenius plot — retain (or incorporate into three-panel summary, Figure 4).

::: {.skill}
**You should be able to:** Explain why the NO oxidation reaction has a negative apparent activation energy, and why negative apparent E_a implies a multi-step mechanism.
:::

---

## 9. Non-Arrhenius Behaviour: Curved Arrhenius Plots as Mechanistic Information

**Intent:** Move beyond straight Arrhenius plots. Curvature is not a nuisance — it is mechanistic information. Two distinct causes.

### 9a. Competing pathways

- When two parallel pathways with different activation energies contribute to the overall rate, k_obs = k₁ + k₂.
- At low T, the low-E_a pathway dominates; at high T, the high-E_a pathway takes over.
- The Arrhenius plot shows two approximately linear regions with different slopes, connected by a curve.
- **Figure (exists):** Curved Arrhenius from competing pathways — retain/update for visual consistency with Figure 5.

### 9b. Change of rate-limiting step

- **The example:** A → B → P (consecutive mechanism from L4).
- The exact solution for [P]_t is biexponential (students have seen this in L4):

  [P]_t = [A]₀[1 − (k₂ exp(−k₁t) − k₁ exp(−k₂t))/(k₂ − k₁)]

- This is *not* simple first-order kinetics — there is no exact single k_obs. But at long times, the faster exponential dies away and the kinetics are dominated by the slower rate constant:
  - k₁ ≪ k₂: [P]_t ≈ [A]₀(1 − exp(−k₁t)), so k_obs ≈ k₁ (step 1 is RDS)
  - k₂ ≪ k₁: [P]_t ≈ [A]₀(1 − exp(−k₂t)), so k_obs ≈ k₂ (step 2 is RDS)
- If E_a,1 ≠ E_a,2, the identity of the slower step changes with temperature. On an Arrhenius plot, ln k₁ and ln k₂ are straight lines with different slopes — they cross at some temperature T*. Below T*, one step is the bottleneck; above T*, the other is.
- The observed Arrhenius plot tracks whichever rate constant is smaller at each temperature, with a smooth curve connecting the two regimes near T*.
- **Note for prose:** In the crossover region near T*, the kinetics are genuinely biexponential — a single-exponential fit is approximate there. This is itself an observable: an experimentalist might notice that the product appearance curve does not fit a single exponential cleanly at intermediate temperatures. This is the signature of comparable rate constants, and it produces the curvature in the Arrhenius plot.
- **Figure 5 (new, essential):** RLS crossover Arrhenius plot. See detailed spec in Figures section. Generated by simulating what an experimentalist would actually measure: for each T, compute the exact [P]_t, then fit to [P]_t = [A]₀(1 − exp(−k_obs t)) assuming pseudo-first-order kinetics. Plot ln k_obs vs 1/T.

**Closing insight (closes the L11 narrative arc):** A curved Arrhenius plot is information, not noise. It tells you something about the mechanism — either that there are competing pathways, or that the identity of the rate-determining step shifts with temperature. More broadly, temperature dependence complements concentration dependence as a probe of reaction mechanisms: concentration data give us the rate law; the rate law constrains the mechanism; temperature data reveal the energy barriers underlying the elementary steps and test mechanistic proposals.

**Close the L1 question:** In L1 we asked how temperature affects reaction rates. The Arrhenius equation captures the pattern; the Boltzmann distribution explains the exponential form; and the details — the sign, magnitude, and curvature of the Arrhenius plot — encode information about the energy landscape and mechanism of the reaction.

**Forward look (one sentence):** Transition state theory, which you will meet in Year 2, takes this further by connecting both A and E_a to molecular properties of the transition state itself.

---

## 10. Key Concepts

- The **Arrhenius equation**, k = A exp(−E_a/RT), is an empirical relationship that describes how rate constants depend on temperature, applying across a huge range of chemical systems.
- An **Arrhenius plot** (ln k vs 1/T) gives a straight line with slope −E_a/R and intercept ln A. The **two-temperature formula** allows determination of E_a from measurements at two temperatures, or prediction of k at a new temperature.
- Reactions generally require energy because bond rearrangement passes through a high-energy **transition state** — a geometric configuration higher in energy than either reactants or products.
- The exponential dependence on 1/T reflects the **Boltzmann distribution**: the fraction of molecules with energy exceeding a threshold is dominated by a factor exp(−E/RT). This is a universal feature of thermal equilibrium, familiar from spectroscopy and kinetic theory.
- For a **single elementary step**, E_a corresponds to the barrier height and A to the rate of attempts. For a **bimolecular** step, A reflects collision frequency × orientation probability; for a **unimolecular** step, A reflects the rate of vibrational energy redistribution into the reactive mode.
- For an asymmetric reaction, E_a,f − E_a,r = ΔE, and K = k_f/k_r — rate constants are constrained by thermodynamics (**detailed balance**).
- For **multi-step mechanisms**, the measured E_a and A are composites that do not correspond to single microscopic barriers or attempt frequencies.
- A **negative apparent E_a** is impossible for a single elementary step and therefore implies a multi-step mechanism. A **curved Arrhenius plot** can indicate competing pathways or a change in the rate-limiting step with temperature. Both are mechanistic diagnostics.

---

## Figures

### Summary table

| # | Figure | Section | Status | Priority |
|---|--------|---------|--------|----------|
| 1 | H + H–H symmetric energy profile | 3a | **New** | Essential |
| 2 | H–H + Br asymmetric energy profile | 5a | **New** | Essential |
| 3 | Maxwell–Boltzmann energy distribution at two T | 4b | **New** | Essential |
| 4 | Three-panel Arrhenius plot summary (positive / ~zero / negative slope) | 8 | **New** | Nice-to-have |
| 5 | RLS crossover Arrhenius plot | 9b | **New** | Essential |
| 6 | Arrhenius plot (straight line) | 2b | **Exists** | Retain |
| 7 | k vs T for different E_a | 2b | **Exists** | Retain |
| 8 | Negative E_a Arrhenius plot | 8c | **Exists** | Retain (may be superseded by #4) |
| 9 | Curved Arrhenius (competing pathways) | 9a | **Exists** | Update for visual consistency with #5 |
| 10 | Reaction coordinate (generic) | — | **Exists** | Superseded by #1 and #2 |

### Detailed figure specifications

**Figure 1: H + H–H symmetric energy profile (Section 3a) — NEW, essential**

Key figure for "why barriers exist."
- Energy on y-axis, reaction coordinate on x-axis.
- Reactants (H + H–H) and products (H–H + H) at the same energy level (ΔE = 0).
- Transition state [H···H···H] at the top of the barrier.
- Barrier height clearly labelled — but **not** labelled as E_a (that identification comes in Section 4c).
- Small molecular diagrams at three points along the coordinate: H far from H–H → H···H···H symmetric → H–H far from H. These connect "position on the reaction coordinate" to "what the atoms are actually doing."
- Pair with Figure 2 as panels (a) and (b) of a single figure.

**Figure 2: H–H + Br asymmetric energy profile (Section 5a) — NEW, essential**

- Same format as Figure 1 but with reactants and products at different energy levels.
- E_a,f and E_a,r both labelled, with ΔE clearly indicated.
- Visually paired with Figure 1 (side-by-side panels) so students see exactly what changes when symmetry is broken.

**Figure 3: Maxwell–Boltzmann energy distribution (Section 4b) — NEW, essential**

The "fraction with enough energy" figure.
- Two distribution curves at clearly labelled temperatures (T₁ and T₂, with T₂ > T₁).
- Vertical line at threshold energy, labelled generically as "threshold energy" or E* (not E_a). The identification of this threshold with the Arrhenius activation energy is made in the text of Section 4c, which follows the figure. Labelling it E_a in the figure would pre-empt the argument.
- Area to the right of the threshold shaded for both curves — visibly larger at T₂.
- Axes: probability (or fraction of molecules) vs translational kinetic energy.
- Present as the Maxwell–Boltzmann KE distribution students have seen in kinetic theory. It is used as an *illustration* of the general Boltzmann principle, not as the only case — the text must make this clear.
- **Placement:** This figure belongs in Section 4b, before the identification in 4c. The text in 4c then says: "the threshold energy in Figure 3 is precisely the activation energy E_a."

**Figure 4: Three-panel Arrhenius plot summary (Section 8) — NEW, nice-to-have**

- Three small Arrhenius plots side by side: (a) negative slope (positive E_a), (b) near-zero slope (E_a ≈ 0), (c) positive slope (negative apparent E_a).
- Each panel labelled with the regime and a brief descriptor.
- If made, the standalone negative-E_a plot (Figure 8) may become redundant.

**Figure 5: RLS crossover Arrhenius plot (Section 9b) — NEW, essential**

The most novel figure. Generated by numerical simulation of what an experimentalist would actually measure.

Procedure:
1. Choose Arrhenius parameters: E_a,1 = 30 kJ mol⁻¹, E_a,2 = 80 kJ mol⁻¹, A₁ = 10⁸ s⁻¹, A₂ = 10¹⁴ s⁻¹. These give a crossover at T* ≈ 435 K (verified: T* = (E_a,1 − E_a,2)/(R ln(A₁/A₂)) ≈ 435 K).
2. For each temperature in a range spanning both regimes (e.g. 300–600 K):
   - Compute k₁(T) and k₂(T) from their Arrhenius equations
   - Generate the exact [P]_t from the biexponential solution over a suitable time range
   - Fit [P]_t = [A]₀(1 − exp(−k_obs t)) — a single-exponential pseudo-first-order fit, as an experimentalist would do
   - Record k_obs
3. Plot ln k_obs vs 1/T (solid curve), overlaid with ln k₁ and ln k₂ individually (dashed lines).

Figure elements:
- Two dashed straight lines: ln k₁ and ln k₂ with different slopes.
- Solid curve: the empirical k_obs extracted from simulated data at each T.
- Crossover point clearly marked.
- Limiting slopes annotated (matching the individual k lines).
- Labels: "step 2 is RDS" (low T), "step 1 is RDS" (high T).
- Near the crossover, the single-exponential fit is imperfect — the k_obs curve smoothly interpolates rather than sharply switching. This is the curvature that an experimentalist would observe.

**Implementation note:** The fitting should use the long-time portion of [P]_t (e.g. from t = 3/k_fast onwards, where the fast exponential has decayed to < 5%) to mimic what an experimentalist would do — they would not typically have access to the very early kinetics where the biexponential character is most visible.

### Figures not recommended

**Composite E_a energy diagram (Section 7):** A two-step energy landscape risks oversimplifying the point. The algebraic argument (E_a,obs = E_a,1 + E_a,2 − E_a,−1) with the derivation is clear enough.

**Pre-exponential factor illustration (Section 6):** The argument is qualitative and verbal. A figure would give it false precision.

---

## Implementation notes

### Sections likely to be lecture vs. notes-only

All sections belong in the notes. For the lecture itself (~50 min), Sections 5 and 6 are the most compressible: Section 5 could be covered as "figure + one key equation"; Section 6 could be summarised briefly rather than developed. The full treatment remains in the notes for students to read.

### In-lecture practice

The course design spec allocates ~10 min for in-lecture Arrhenius analysis. The N₂O₅ worked example in Section 2c is worked through in the notes; in the lecture, a second dataset could be presented for students to attempt (e.g. "here are k values at three temperatures — construct the Arrhenius plot and extract E_a"). Resolve at slide-design stage, but the notes should provide enough worked examples that students can practise independently.

### Equation labelling plan

Equations that need `(\#eq:label)` for cross-referencing:

| Label | Equation | First appears | Referenced from |
|---|---|---|---|
| `eq:arrhenius` | k = A exp(−E_a/RT) | 2a | Throughout |
| `eq:arrhenius-linear` | ln k = ln A − (E_a/R)(1/T) | 2b | 2c (two-T derivation) |
| `eq:two-temperature` | ln(k₂/k₁) = (E_a/R)(1/T₁ − 1/T₂) | 2c | Worked example, possibly Section 8 |
| `eq:barrier-constraint` | E_a,f − E_a,r = ΔE | 5a | 5b, 8c |
| `eq:ea-composite` | E_a,obs = E_a,1 + E_a,2 − E_a,−1 | 7b | 8c (negative E_a) |

The [P]_t biexponential (Section 9b) does not need a label — it is presented for analysis, not cross-referenced. Use `align*` or `$$` for unnumbered display equations (derivation steps, intermediate results).

### Known pitfalls for prose conversion

1. **Section 1:** Frame as scientific observation, not course recap. The opening should land on the question "is there a pattern in k(T)?" not on "we haven't covered temperature yet."
2. **Section 2a:** Acknowledge that the name "activation energy" anticipates the physical picture.
3. **Section 3:** State the naive expectation (why don't reactions just happen?) before explaining barriers.
4. **Section 4a:** When switching from k_BT (per-molecule Boltzmann factor) to RT (molar Arrhenius equation), explain the conversion explicitly.
5. **Section 4b:** Be specific about what the M–B figure shows (translational KE distribution), then step back to the general principle.
6. **Section 4c:** State the assumption that the dominant temperature dependence is the energy factor. This is a justification, not a derivation.
7. **Section 5b:** Note briefly that K = exp(−ΔG°/RT) in general; this energy-only picture neglects entropy. Appropriate simplification for Y1.
8. **Section 7b:** Show the key algebraic step (d(ln k_obs)/d(1/T)) so the result feels earned.
9. **Section 8c:** State explicitly why microscopic barriers must be ≥ 0 (a transition state lower in energy than reactants would not be a barrier).
10. **Section 9b:** Do not claim any analytical formula for k_obs. The approach is fully numerical: simulate the exact [P]_t, fit pseudo-first-order, plot the empirical k_obs. The text develops the limiting cases analytically (k_obs → min(k₁, k₂)) and the figure shows what an experimentalist would actually observe. The harmonic mean k₁k₂/(k₁ + k₂) may be mentioned as an approximation if useful, but it is not the primary result.
11. **Callbacks:** Each callback (L1, L3, L4–5, L7) should be a brief clause, not a digression.
12. **Terminology:** Use "transition state" consistently throughout. Define once in Section 3a.
13. **Section 4b → 4c transition:** Note that the Boltzmann argument does not depend on the *source* of the barrier — it works for any energy threshold, not just the bond-rearrangement barriers of Section 3.
14. **Aside candidates:** The Evans–Polanyi correlation (5a) and the ΔG° vs ΔE caveat (5b) may work better as `#### Aside: {-}` blocks if they interrupt the main flow. Judge at implementation.

### Estimated timing (lecture delivery)

| Section | Notes | Lecture |
|---------|-------|---------|
| 1. Opening | ~1 page | ~2 min |
| 2. Arrhenius equation | ~3 pages | ~12 min |
| 3. Energy barriers | ~2 pages | ~7 min |
| 4. Boltzmann factor | ~2 pages | ~7 min |
| 5. Forward/reverse | ~1.5 pages | ~3 min (compressed) |
| 6. Pre-exponential | ~1.5 pages | ~3 min (compressed) |
| 7. Composite E_a | ~1.5 pages | ~5 min |
| 8. Three regimes | ~1.5 pages | ~4 min |
| 9. Non-Arrhenius + closing | ~2 pages | ~7 min |
| **Total** | **~16 pages** | **~50 min** |

### Style guide checklist (verify at implementation)

- [ ] Voice is conversational but authoritative
- [ ] Chapter opens with contextual paragraph (not a list)
- [ ] Chapter closes with Key Concepts summary
- [ ] Skill statements clarify examinable derivations and calculations
- [ ] Physical interpretation accompanies mathematical derivations
- [ ] Equations use `\mathrm{d}` for derivatives and `\mathrm{}` for chemical species
- [ ] Important equations are numbered and labelled
- [ ] Figures have detailed, self-contained captions
- [ ] Chemical subscripts use `~subscript~` syntax in prose
- [ ] British spelling throughout
- [ ] Limiting cases are analysed where appropriate
- [ ] Connections to other chapters are explicit
- [ ] Paragraphs are short (2–4 sentences)
- [ ] Derivations are complete before interpretation begins
- [ ] No signposting or meta-narrative in prose
- [ ] All notation used more than once; all numbered equations are referenced
- [ ] Terminology consistent ("transition state" throughout)

---

## Changes relative to v7

| v7 | v8 | Reason |
|----|-----|--------|
| "Narrative move:" annotations throughout | Replaced with "Intent:" authorial notes + "Pitfall for prose:" warnings | Clearer distinction between structural intent and prose-conversion guidance |
| E_a named "activation energy" without comment in 2a | Explicit note that the name anticipates the physical picture | Consistent with empirical-first philosophy |
| Section 3 does not state naive expectation | Naive expectation stated explicitly: "if products are lower in energy, why don't molecules just convert?" | Needed to motivate the barrier concept |
| Section 4a: "fraction... proportional to exp(−E/k_BT)" stated as general principle | Reworded: probability of a state ∝ exp(−E/k_BT); fraction exceeding threshold *dominated by* exponential factor | More precise; avoids conflating exact Boltzmann distribution with integrated tail |
| Section 4b: collision-energy case described vaguely | Specific: this is the M-B translational KE distribution; used as illustration of general principle; prose must step back explicitly | Prevents students thinking argument is specific to gas-phase collisions |
| Section 4c: rate ∝ (attempts) × (fraction) stated without qualification | Assumption stated explicitly: dominant T-dependence is from energy factor; attempt frequency weakly T-dependent | Prevents students thinking Arrhenius is derived from first principles |
| Section 5b: K = (A_f/A_r) exp(−ΔE/RT) without caveat | Note added: energy-only picture; ΔG° in general | Prevents confusion with thermodynamics course |
| Section 7b: E_a,obs = E_a,1 − E_a,−1 + E_a,2 stated | Derivation step shown (d(ln k_obs)/d(1/T)) | Result feels earned |
| Section 8c: "all microscopic barriers are ≥ 0" stated without argument | Argument given: transition state lower than reactants would not be a barrier | Supports the claim used as diagnostic |
| Section 9b: "Under SSA: k_obs = k₁k₂/(k₁ + k₂)" | Corrected: exact biexponential solution; k_obs ≈ min(k₁, k₂) in limits; harmonic mean as approximation from mean reaction time; figure generated numerically | SSA attribution was incorrect; new treatment is more honest and connects to L4 |
| Section 10: standalone course synthesis section | Removed as standalone section; closing paragraph integrated into end of Section 9 | Avoids anticlimactic recap; closes L11 arcs without becoming a course summary |
| Key Concepts: 10 bullets | Consolidated to 8 | Style guide recommends 4–8 |
| Terminology varies: "transition point," "intermediate configuration," "transition state" | "Transition state" used consistently; defined in Section 3a | Consistency |
| R vs k_B switch implicit | Explicit note to convert in prose | Prevents confusion |
| No implementation notes | Full section: prose pitfalls, timing, style checklist, lecture vs notes guidance | This is a planning document for implementation |
