# Review: `lecture_09.Rmd` (L9: Chain Reactions) — Second Pass

**Reviewer:** Claude
**Date:** 2026-03-11
**Status:** Read-only review of revised version — no changes made to source file

## Overall Assessment

The revised lecture is substantially improved. The opening paragraph now makes concrete backward connections to the SSA and poses the central question ("how much damage does it do?") upfront. The chain length section has been reworked from first principles via a probability argument, with explicit rate expressions and cancellations that make the derivation transparent. The new ozone-specific figures (linear chain and cycle) replace a generic diagram with concrete illustrations of the mechanism under discussion. The [M] notation inconsistency, the missing Evans–Polanyi premise, the dangling fragment, and the figure-ordering issue are all resolved. The remaining issues are minor: em dash overuse, three residual signposting phrases, a figure that interrupts a sentence–equation pair, and two small imprecisions in the chain length prose.

## Section-by-Section Review

### Opening paragraph (line 3)

All three jobs well done: backward connection to the SSA is concrete ("write rate equations for multi-step mechanisms and use the SSA to derive overall rate laws"), the concept of regeneration is introduced clearly, and the central question is posed at the end ("how much damage does it do along the way?"). A strong opening. ✓

### Section: The Ozone Layer and CFC-Catalysed Destruction (lines 5–45)

**Figures (criterion 6):** All three figures (`ozone-hole`, `ozone-chain`, `ozone-cycle`) are referenced before they appear. ✓

**Figure interrupting prose (criterion 10/pacing):** Line 29 ends with "The net reaction is:" — but the `ozone-chain` figure (lines 31–33) intervenes before the net reaction equation at line 35. A reader encountering "The net reaction is:" expects the equation immediately; the figure breaks this expectation. The figure reference at "forming a self-sustaining chain (Figure \@ref(fig:ozone-chain))" is earlier in line 29, so the figure could be placed *before* the sentence about the net reaction without disrupting the reference order.

**Voice (criterion 9):** Reads well throughout. The prose flows naturally from mechanism to definitions to the closing question. ✓

### Section: The H₂ + Br₂ Reaction (lines 47–95)

**Stepwise argument (criterion 14):** Naive expectation explicitly stated at line 53 ("we might expect a straightforward rate law such as ν = k[H₂][Br₂]"). Mechanism presented as established science. Bond energy arguments support the claim about relative rate constants. All good. ✓

**Evans–Polanyi premise (criterion 13):** The justification added in the earlier round ("For closely related reactions that involve the same type of bond-forming step, exothermic reactions tend to have lower activation barriers than endothermic ones") remains in place at line 91. ✓

**Signposting (criterion 4):** Line 60: "To understand where this rate law comes from, we need to consider the full chain mechanism." — This announces intent rather than proceeding. Could be trimmed or removed.

**Figures (criterion 6):** `hbr-chain` referenced at line 77 before line 79. `hbr-chain-cycle` referenced at line 91 before line 93. Both correct. ✓

### Section: Deriving the Rate Law Using the SSA (lines 97–150)

**Notation (criterion 15):** [M] absorption stated at line 99, consistently maintained throughout the derivation and chain length section. ✓

**Mathematical accuracy:** SSA derivation, cancellation, steady-state concentrations, and final rate law are all correct. ✓

**Intuition (criterion 3):** Physical interpretation follows each key result: the meaning of the cancellation (line 119), the origin of [Br₂]^{1/2} (line 126), the inhibition term (line 148), and the limiting cases (line 150). ✓

**Dangling referent (criterion 15):** "This self-inhibition and the concept of negative apparent orders are explored further in Appendix..." — clear referent. ✓

### Section: Chain Length (lines 152–184)

This section is substantially improved. The probability motivation (lines 154–156) gives physical intuition before the rate-ratio equation. The explicit cancellation in the HBr chain length (line 174) is transparent. The substitution to measurable quantities (line 178) completes the derivation. The new material on the general chain length with inhibition (lines 180–184) connects the chain length to the rate law and provides genuine physical insight.

**Notation used once (criterion economy):** Line 156 introduces $p(\text{propagation})$ and $p(\text{termination})$, which appear only in this one equation. The style guide notes: "Don't introduce notation that appears only once." Since the $p$-notation serves to motivate the rate ratio on the next line, it is pedagogically useful but technically violates the economy principle. Consider whether the probability argument could be made in prose without the intermediate equation.

**Imprecise language (criterion 13):** Line 180: "propagation must now compete with both termination *and* inhibition for the fate of each radical." This is slightly imprecise. Inhibition competes with the *second* propagation step for H•, while termination competes with the *first* propagation step for Br•. Different radicals face different competing pathways. The formula at line 182 is correct, but the prose oversimplifies by suggesting all three fates apply to every radical.

**Imprecise qualification (criterion 13):** Line 184: "Since the rate of initiation ($k_1[\mathrm{Br_2}]$) is approximately constant" — true only while [Br₂] has not changed significantly. A qualifying phrase ("early in the reaction" or "while [Br₂] has not been substantially consumed") would sharpen this.

**Voice (criterion 9):** Line 165: "Note that at steady state, the rate of initiation equals the rate of termination" — "Note that" is flagged as a mild signpost opener by criterion 9.

### Subsection: Returning to Ozone (lines 186–208)

**Stepwise argument (criterion 14):** The naive expectation is now explicit (line 202: "If termination permanently removed the radical, this chain length of ~10² would represent the total ozone destruction per chlorine atom"). The surprise follows naturally. ✓

**Scientific precision (criterion 13):** "Chlorine-containing species" with parenthetical listing of forms (line 206) is accurate. ✓

**Explicit cancellation (line 194):** Showing both [Cl•] in the ratio before cancelling makes the contrast with HBr (where [Br•] does not fully cancel) transparent. Good addition. ✓

### Closing paragraph, skill statements, and Key Concepts (lines 210–222)

**Signposting (criterion 4):** Line 210: "In the next lecture, we will see what happens when propagation steps produce *more* intermediates than they consume — leading to **branching chains** and explosions." This is an explicit forward reference ("In the next lecture, we will see..."). The style guide and criterion 10 note that the closing should circle back to the questions or ideas from the opening, providing narrative closure, rather than previewing the next lecture. The preceding material (ozone chain length, reservoir species, straight chains) does circle back to the opening question and provides good closure. This final sentence slightly weakens the narrative by looking forward rather than landing on the completed argument.

**Key Concepts (lines 216–222):** Five bullets, well written. The final bullet no longer includes a forward reference about branching. ✓

**Skill statement (lines 212–214):** Comprehensive and appropriately targeted. ✓

## Cross-Cutting Issues

1. **Em dashes:** 9 em dashes in approximately 2,540 words of prose = 1 per ~282 words. This exceeds the guideline of ~1 per 500 words. The formatting is consistent (all spaced ` — `). No em dashes are used for numeric ranges and none are paired constructions that would work better as parentheses. The overuse is modest and each individual em dash reads naturally, but the cumulative density gives the prose a slightly breathless quality.

2. **Three residual signposting instances:** Lines 60, 165, and 210 (detailed above).

3. **The [M] notation inconsistency** from the first version is fully resolved. ✓

4. **Figure `ozone-chain` interrupts** the "The net reaction is:" → equation flow (line 29 → 31–33 → 35).

## Narrative Coherence Assessment

### Lecture level

The central theme — chain reactions feature regeneration of intermediates, and the chain length quantifies the damage — is stated clearly in the opening and developed systematically through two examples of increasing complexity. The arc is:

1. Opening: What is a chain reaction? How much damage can one radical do?
2. CFC/ozone: Concrete motivating example; introduces initiation, propagation, termination.
3. HBr: More complex chain with inhibition; SSA derivation reproduces the experimental rate law.
4. Chain length: Quantifies the competition between propagation and termination; returns to ozone; reveals the reservoir species surprise.
5. Closing: Defines straight chains; bridges to branching chains.

The opening question is answered quantitatively in the ozone chain length section. The reservoir species discussion adds a genuine narrative twist. The lecture achieves strong closure *before* the final forward-looking sentence at line 210.

### Section level

All section transitions are motivated by content: the move from ozone to HBr is motivated by the need for a more complex example; the chain length section is motivated by the quantitative question posed at the end of the ozone section; the return to ozone is motivated by the chain length tools just developed. The only procedural transition remaining is at line 60 ("To understand where this rate law comes from, we need to consider the full chain mechanism"), which could be trimmed.

The chain length section's new structure (probability → rate ratio → HBr → ozone) builds clearly from intuition to application. The addition of the general chain length with inhibition (lines 180–184) is pedagogically valuable: it connects the chain length to the rate law and provides the insight that "the rate slows down precisely because the chains are getting shorter."

## Systematic Verification Passes

### Pass 1: Imprecise scientific language (criterion 13)

| Location | Issue | Severity |
|----------|-------|----------|
| Line 180 | "propagation must now compete with both termination *and* inhibition for the fate of each radical" — oversimplifies; different radicals face different competing pathways | Minor |
| Line 184 | "Since the rate of initiation ($k_1[\mathrm{Br_2}]$) is approximately constant" — true only early in the reaction; needs qualification | Minor |

The imprecise language issues from the first review (line 87's Evans–Polanyi assertion, "slow" for initiation, "chlorine atom" for chlorine-containing species) are all resolved. ✓

### Pass 2: Dangling referents (criterion 15)

No paragraph-opening "it", "this", "these", or "that" with ambiguous referents found. The dangling fragment "starting a new chain" from the first version is resolved (now part of the preceding sentence at line 202). ✓

### Pass 3: Notation consistency (criterion 15)

| Item | Status |
|------|--------|
| [M] convention (absorbed into k₁, k₄) | Consistent throughout ✓ |
| ν̄ (chain length) vs ν (reaction rate) | Distinguished by overbar; no confusion ✓ |
| p(propagation)/p(termination) at line 156 | Used only once; not referenced again |
| k₂, k₃, k₄ reused for ozone (lines 186–194) | These are different rate constants from the HBr mechanism, but this is conventional (each mechanism has its own k values). The ozone mechanism uses k₂ and k₄ from its own definitions (Section \@ref(sec:ozone)). No student confusion expected since the mechanisms are discussed in separate sections. ✓ |

### Pass 4: Unnecessary emphasis (criterion 12)

| Location | Text | Verdict |
|----------|------|---------|
| Line 3 | *regenerated* | Justified — key concept |
| Line 119 | *total* | Justified — disambiguates |
| Line 126 | *second order* | Justified — highlights the key mechanism |
| Line 176 | *second order* | Justified — parallel structure with previous use |
| Line 180 | *and* | Justified — emphasises the new competitor |
| Line 184 | *because* | Borderline — the content demonstrates the claim, so the emphasis is not strictly necessary. Minor. |
| Line 210 | *more* | Justified — key distinction between straight and branching |

### Pass 5: Naive expectation stated? (criterion 14)

| Location | Claim | Naive expectation stated? |
|----------|-------|--------------------------|
| Lines 53–58 | HBr rate law is complex | **Yes.** "we might expect a straightforward rate law such as ν = k[H₂][Br₂]" ✓ |
| Lines 200–202 | Chain length ~10² falls short of ~10⁵ | **Yes.** "If termination permanently removed the radical, this chain length of ~10² would represent the total ozone destruction per chlorine atom." ✓ |

### Em dash count

9 em dashes in ~2,540 words of prose ≈ 1 per 282 words. Exceeds the ~1 per 500 words guideline.

| Line | Usage |
|------|-------|
| 3 | "removes it — but how much" |
| 27 | "stable molecules — this is" |
| 37 | "permanently — here by converting" |
| 64 | "intermediates — bromine radicals" |
| 150 | "defined — but in the limit" |
| 184 | "shrinks — each successive chain" |
| 198 | "completely — because both" |
| 208 | "developed — writing a mechanism" |
| 210 | "consume — leading to" |

All are consistently formatted (spaced ` — `). No paired constructions or numeric ranges. ✓

## Prioritised Recommendations

### Should fix

1. **Reposition Figure `ozone-chain` to avoid interrupting the "net reaction" sentence (lines 29–35).** Currently, "The net reaction is:" is followed by the figure, then the equation. Move the figure to *after* the net reaction equation (or earlier, before the "Each turn of the cycle..." sentence) so that the text flows directly into the equation it introduces.

2. **Reduce em dash count.** Nine em dashes in ~2,540 words is above the recommended density (~1 per 500 words). Candidates for replacement:
   - Line 27: "stable molecules — this is the **initiation** step" → "stable molecules; this is the **initiation** step" (or restructure)
   - Line 64: "intermediates — bromine radicals ($\mathrm{Br}^{\bullet}$) and hydrogen radicals ($\mathrm{H}^{\bullet}$)" → "intermediates, bromine radicals... and hydrogen radicals..." (parenthetical listing suits a colon or comma better)
   - Line 198: "cancels completely — because both propagation and termination are first order" → "cancels completely, because both..."
   - Line 208: "developed — writing a mechanism" → "developed (writing a mechanism..." with matching closing parenthesis)
   Reducing from 9 to 5 would bring the density to ~1 per 508 words, within guidelines.

3. **Remove the forward reference at line 210.** "In the next lecture, we will see what happens when propagation steps produce *more* intermediates than they consume — leading to **branching chains** and explosions." This announces future content rather than providing closure. The preceding material (straight chain definition, ozone example of cumulative damage) makes a strong closing point on its own. Consider ending at "even this steady balance can cause enormous cumulative damage" (or a similar reworked sentence that lands on the completed argument), and letting the concept of branching chains await L10's own opening.

4. **Remove residual signposting at line 60.** "To understand where this rate law comes from, we need to consider the full chain mechanism." — Announces intent. The preceding paragraph (unusual features of the rate law, cannot arise from a single step) already motivates the mechanism. This sentence can be deleted or the transition made implicit by proceeding directly to "### The Mechanism."

### Minor

5. **Sharpen the inhibition-competition language (line 180).** "Propagation must now compete with both termination *and* inhibition for the fate of each radical" oversimplifies: Br• faces propagation vs termination, while H• faces propagation vs inhibition. Consider: "Each radical now faces a competing pathway: H• can either propagate (reacting with Br₂) or be diverted by inhibition (reacting with HBr), while Br• continues to face propagation vs termination." Or more concisely: "The inhibition step competes with propagation for H•, reducing the fraction of cycles that form product."

6. **Qualify "approximately constant" at line 184.** "Since the rate of initiation ($k_1[\mathrm{Br_2}]$) is approximately constant" — add "early in the reaction" or "while [Br₂] has not been substantially consumed" to make the approximation's domain explicit.

7. **Replace "Note that" at line 165.** "Note that at steady state, the rate of initiation equals the rate of termination" — "Note that" is a mild signpost. Consider: "At steady state, the rate of initiation equals the rate of termination ($\nu_\mathrm{init} = \nu_\mathrm{term}$), so the chain length is equivalently $\nu_\mathrm{prop}/\nu_\mathrm{init}$."

8. **Consider removing the intermediate probability equation at line 156.** The $p(\text{propagation})/p(\text{termination})$ notation is introduced and used only once — the next equation (Eqn. \@ref(eq:chain-length)) replaces it with rate notation. The probability argument could be made in prose ("The chain length depends on the relative likelihood of these two fates; since probability is proportional to rate...") without a standalone equation. This is a judgment call: the equation adds visual clarity but introduces notation that is immediately discarded.
