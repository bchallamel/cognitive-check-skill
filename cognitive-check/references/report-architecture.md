# Cognitive Check Report Architecture

Use this reference when producing a full cognitive check, planning a visual report, or needing the detailed contract behind the skill.

## Operating Principles

- Separate truth from reasoning quality: true claims can support bad reasoning, and uncertain claims can still be intellectually honest.
- Prioritize consequential claims over decorative claims when the artifact is long or complex.
- Distinguish fatal defects, meaningful uncertainty, normal incompleteness, and easy-to-fix weaknesses.
- Treat values, goals, tradeoffs, incentives, and emotional pressure as part of cognition.
- Avoid false precision. Do not use confident tags or ratings when the evidence work does not justify them.
- Make the user better at the next round of thinking, not only better informed about this artifact.

## Trust Stance Definitions

| Stance | Meaning |
| --- | --- |
| Ready | The artifact is sufficiently grounded and reasoned for the user's stated purpose. |
| Use With Caveats | The artifact is usable, but limitations should be preserved or disclosed. |
| Verify First | The artifact may be usable, but key claims or assumptions need checking first. |
| Major Revision | The artifact has substantial reasoning, sourcing, framing, or scope problems. |
| Do Not Use | The artifact is contradicted, misleading, incoherent, unsafe for the goal, or too unreliable to support action. |

## Full Report Structure

1. Stable opening overview
2. Intake and context
3. Claim triage and validation
4. Argument map
5. Evidence and source audit
6. Cognitive diagnostic
7. Explorative sources
8. Alternative hypotheses
9. Assumption ledger
10. Calibration and change conditions
11. Upgrade plan

## Intake and Context

Capture:

- Artifact type: memo, essay, source packet, plan, deck, transcript, report, strategy, policy, claim list, or other
- User relationship to artifact: produced, received, co-created, or unknown
- User goal: understand, publish, decide, challenge, revise, respond, invest, teach, persuade, or other
- Stakes: low, medium, high, or unknown
- Error cost: what would be worse, false confidence or false skepticism
- Time horizon: immediate decision, near-term revision, long-term knowledge, or unknown
- Verification depth: internal-only, source-aware, external fact-check, or research-grade

## Claim Priority

Use these priority levels when helpful:

| Priority | Meaning |
| --- | --- |
| Load-bearing | If wrong, the main conclusion or decision collapses. |
| Risk-bearing | If wrong, the user may suffer meaningful practical, reputational, legal, financial, health, or relational harm. |
| Credibility-bearing | If wrong, the artifact's trustworthiness is damaged. |
| Framing-bearing | Shapes how the reader interprets the issue, even if not directly factual. |
| Decorative | Adds color or emphasis but does not materially change the argument. |

## Argument Map Contract

Represent the argument in a compact structure:

```markdown
Main conclusion:
- ...

Premises:
- P1: ...
- P2: ...

Evidence:
- E1 supports P1: ...
- E2 supports P2: ...

Warrants:
- W1: The argument assumes ...

Objections addressed:
- ...

Objections missing:
- ...

Missing links:
- ...
```

For later visual rendering, preserve node types:

- Conclusion
- Premise
- Evidence
- Warrant
- Objection
- Missing link

## Evidence and Source Audit

Assess:

- Source quality: primary versus secondary, expertise, method, reputation, and transparency
- Source independence: whether sources genuinely corroborate each other or repeat the same origin
- Source diversity: geography, institution, ideology, method, discipline, stakeholder, or lived experience
- Recency fit: whether newer evidence is necessary, or older evidence is more stable and appropriate
- Method fit: whether the evidence type can support the claim being made
- Evidence chain: whether the path from claim to evidence is traceable
- Missing evidence: what evidence should exist if the claim is true
- Correction posture: whether the artifact acknowledges uncertainty, limitations, or possible error

## Cognitive Diagnostic Dimensions

Use Low, Medium, High, or Not Assessable. Always include signal and implication.

| Dimension | Diagnostic Question |
| --- | --- |
| Confirmation bias | Does the artifact favor evidence that supports its conclusion while minimizing disconfirming evidence? |
| Reactive opposition | Does it overcorrect against a disliked idea, source, institution, trend, person, or prior belief? |
| Missing context | Does it omit background, constraints, definitions, history, incentives, or comparators? |
| Too narrow | Does it reason from too small a sample, timeframe, geography, stakeholder group, or lens? |
| Too sharply contextualized | Does it overfit to one situation and miss broader patterns, transferability, or system implications? |
| Recency bias | Does it overweigh recent examples, news, data, or emotional salience? |
| Source selection quality | Are sources authoritative, relevant, current where needed, primary where possible, and interpreted fairly? |
| Source diversity risk | Does it rely on one source type, ideology, geography, method, institution, or perspective when diversity matters? |
| Assumption load | Does it depend on fragile, hidden, untested, or value-laden assumptions? |
| Causality versus correlation | Does it confuse association, chronology, mechanism, necessity, sufficiency, or causal attribution? |
| Base-rate awareness | Does it compare claims to normal frequencies, historical ranges, category norms, or expected failure rates? |
| Incentive awareness | Does it consider who benefits, who pays, who is omitted, and how incentives may distort interpretation? |
| Counterargument quality | Does it address the strongest opposing explanation rather than weak versions? |
| Uncertainty handling | Does it use calibrated confidence, caveats, ranges, and falsifiability rather than binary certainty? |
| Operational clarity | Does it turn analysis into specific, usable recommendations? |
| Rhetorical pressure | Does it use urgency, fear, status pressure, social proof, identity cues, moral coercion, or false dichotomies to bypass scrutiny? |

## Explorative Sources

Use explorative sources to turn source diversity problems into concrete perspective-broadening moves.

Include this section after cognitive diagnostic and before alternative hypotheses when the artifact would benefit from listening to sources, voices, or evidence streams not represented in the current frame.

| Source Direction | Why It Broadens the View | What To Look For |
| --- | --- | --- |
| Person, stakeholder group, discipline, institution, document type, dataset, or evidence stream. | Bias, blind spot, assumption, or missing context it helps correct. | Questions, claims, evidence, disagreement, or lived experience to seek. |

Useful source directions include:

- Primary stakeholders affected by the artifact's recommendation or framing
- Serious critics of the artifact's position
- Practitioners who live with the operational consequences
- Domain experts from adjacent disciplines
- Primary documents, policies, contracts, standards, or data
- Historical analogues that complicate the artifact's analogy
- International, cultural, class, gender, or minority perspectives when relevant
- Sources with different incentives from the artifact's author or cited authorities

Prefer source directions that change the user's next act of inquiry. Avoid generic "read more research" recommendations.

## Alternative Hypotheses

Use rival explanations to reduce confirmation bias and reactive opposition.

| Alternative Hypothesis | What It Explains | What Would Support It | What Would Weaken It |
| --- | --- | --- | --- |

Do not create fake symmetry. If an alternative is weak, say why.

## Assumption Ledger

Prioritize assumptions that are load-bearing, fragile, hidden, or likely to change the user's decision.

| Assumption | Type | Why It Matters | Confidence | How To Test |
| --- | --- | --- | --- | --- |
| ... | Factual, causal, value, scope, behavioral, strategic, or operational. | ... | Low, Medium, or High. | ... |

## Calibration and Change Conditions

Include:

- Overall confidence: Low, Medium, or High
- Uncertainty sources: missing sources, ambiguous language, outdated data, unverifiable claims, unclear goals, or contested values
- What would change the assessment: evidence, stakeholder input, primary sources, data, definitions, or counterexamples

## Future Visual Report Layer

The first skill version may produce text and tables only, but keep outputs structured enough for later visual conversion.

Anticipated visual components:

- Argument map: node-link diagram showing conclusions, premises, evidence, warrants, objections, and missing links
- Claim validation matrix: table with color-coded check tags and claim priority
- Evidence chain diagram: claim-to-source trace showing evidence depth and source independence
- Source diversity map: grid or radar view of source types, perspectives, methods, geography, and stakeholder coverage
- Explorative sources map: menu of voices, disciplines, documents, and evidence streams to consult next
- Cognitive risk dashboard: compact visual summary of bias and reasoning risks
- Assumption ledger: structured table or priority matrix plotting confidence against impact
- Alternative hypothesis matrix: comparison table or weighted evidence grid
- Upgrade roadmap: prioritized fix sequence by urgency and effort

Do not force graphics into the text-only skill. Preserve stable headings, node types, table columns, and priority levels so a later renderer can convert the report into diagrams.
