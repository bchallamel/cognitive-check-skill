---
name: cognitive-check
description: Cognitive validation of uploaded, pasted, or referenced artifacts, including fact-checking, claim triage, reasoning audits, bias diagnostics, assumption ledgers, source and evidence review, explorative source recommendations, argument mapping, alternative hypotheses, calibration, upgrade recommendations, and optional HTML/PDF report generation. Use when Codex needs to evaluate whether a document, memo, strategy, plan, claim set, deck, transcript, report, recommendation, or draft is trustworthy, well-reasoned, appropriately scoped, honestly uncertain, and ready to use, revise, challenge, publish, or discard.
---

# Cognitive Check

## Overview

Perform a cognitive validation report on a specific artifact. Separate claim truth from reasoning quality, make load-bearing assumptions visible, test for bias and scope errors, and recommend concrete upgrades.

Default to an adaptive report after the opening overview. Produce a full report only when the user asks for a full cognitive check, comprehensive report, complete audit, research-grade review, or similar depth.

For the full architecture, visual-report hooks, and detailed section contracts, read `references/report-architecture.md`.

When the user asks for an HTML report, PDF report, exportable report, shareable document, visual report, or browser-openable report, read `references/report-rendering.md`.

## Intake

If no artifact is available, ask the user to provide the artifact before performing the check.

Before analysis, infer the context needed to judge the artifact well. Ask a clarifying question only when missing context would materially change the assessment.

Capture or infer:

- Artifact type
- User relationship to artifact: produced, received, co-created, or unknown
- User goal: understand, decide, revise, challenge, respond, publish, invest, teach, persuade, or other
- Stakes: low, medium, high, or unknown
- Error cost: whether false confidence or false skepticism is more dangerous
- Time horizon
- Verification depth: internal-only, source-aware, external fact-check, or research-grade

## Stable Opening Overview

Always begin with this exact section structure and order, regardless of artifact complexity:

```markdown
## Cognitive Check Overview

**Trust stance:** Ready | Use With Caveats | Verify First | Major Revision | Do Not Use

**Confidence:** Low | Medium | High

**Useful signals:** 2-4 bullets on what is strong, grounded, clear, generative, or decision-ready.

**Red flags:** 2-4 bullets on what is unsupported, misleading, biased, overconfident, underspecified, inconsistent, manipulative, or risky.

**Recommended next move:** 2-4 bullets on whether to trust, revise, verify, narrow, broaden, source, reframe, challenge, or reject the artifact.

**What would change this assessment:** 1-3 bullets naming evidence, context, source access, definitions, stakeholder input, or counterexamples that would update the judgment.
```

Treat this overview as the user's cognitive dashboard. Keep the headings stable. Keep the content concise and decision-oriented. Do not bury severe concerns in later sections.

## Report Depth

After the stable overview, adapt the remaining report to the user's goal and artifact complexity.

Default adaptive report:

- Include only the sections that materially improve the user's decision or revision path.
- Prioritize load-bearing claims, fragile assumptions, evidence gaps, reasoning failures, and high-value upgrades.
- State when a section is omitted because it is not material or not assessable.
- Offer a fuller pass when the artifact is long, high-stakes, or source-heavy.

Full report:

- Include claim triage and validation.
- Include an argument map.
- Include evidence and source audit.
- Include cognitive diagnostic.
- Include explorative sources.
- Include alternative hypotheses.
- Include assumption ledger.
- Include calibration and change conditions.
- Include upgrade plan.

## Claim Triage and Validation

Extract and evaluate consequential claims first. A consequential claim carries the artifact's argument, decision, credibility, risk, or emotional force.

When feasible, review every meaningful factual, analytical, causal, normative, predictive, or comparative claim. For long artifacts, state that the report prioritizes load-bearing claims and offer exhaustive extraction as a deeper pass.

Use this table:

| Claim | Check | Notes | Upgrades |
| --- | --- | --- | --- |
| Exact or lightly normalized claim. | Status label. | Evidence, uncertainty, source status, reasoning issue, or why it matters. | Better wording, caveat, verification step, or stronger replacement. |

Use the smallest tag set that captures the claim's epistemic status. Prefer one primary tag per claim; put secondary signals in Notes.

| Tag | Meaning |
| --- | --- |
| Verified | Confirmed by reliable evidence available in the artifact, supplied context, or checked sources. |
| Grounded | Well-supported by the artifact's evidence, but not independently verified. |
| Plausible | Reasonable, but not sufficiently evidenced yet. |
| Opinion | Subjective judgment, interpretation, taste, preference, priority, or value claim. |
| Framing | Rhetorical or conceptual lens rather than a directly checkable claim. |
| Incomplete | Missing important context, scope, definitions, evidence, or qualifiers. |
| Unsupported | Asserted without enough evidence or reasoning. |
| Contradicted | Conflicts with evidence in the artifact or reliable external information. |
| Internally Inconsistent | Conflicts with another claim, premise, number, timeline, or conclusion in the artifact. |
| Ambiguous | Too vague, broad, undefined, or semantically unstable to validate cleanly. |
| Overstated | Directionally possible but expressed with too much certainty, scale, or universality. |
| Speculative | Predictive or hypothetical claim presented without adequate uncertainty. |
| Needs Verification | Checkable, but requires external validation before use. |
| Causal Leap | Treats correlation, chronology, or association as causation without support. |
| Quantitative Risk | Uses numbers, rates, samples, rankings, estimates, or measurements that need method scrutiny. |
| Scope Risk | May be true only for a narrower or broader context than the artifact implies. |

Use plain-text labels in Markdown. In rendered HTML or PDF reports, pair the label with an appropriate Lucide icon while preserving the label in text.

Do not label a claim `Verified` unless it has been checked against reliable evidence or is directly established by a trusted source in the supplied artifact.

## Argument Map

Map the reasoning before judging the artifact globally.

Include the main conclusion, supporting premises, evidence, hidden warrants, objections addressed, objections missing, and missing links. Keep the first version compact, but preserve a structure that can later become a visual node-link argument map.

## Evidence and Source Audit

Evaluate whether the evidence base is fit for the artifact's claims and purpose.

Check source quality, source independence, source diversity, recency fit, method fit, evidence-chain traceability, missing evidence, and correction posture.

When useful, use this table:

| Evidence or Source | Role in Argument | Quality | Independence | Fit | Notes |
| --- | --- | --- | --- | --- | --- |

Use external verification when the user asks for fact-checking or when claims involve current facts, law, medicine, finance, product capabilities, company leadership, prices, policy, or recent events.

If browsing or source access is unavailable, do not pretend to verify externally. Use `Grounded`, `Plausible`, `Needs Verification`, `Unsupported`, or `Incomplete`.

## Cognitive Diagnostic

Evaluate how the artifact thinks, not only whether individual claims are true.

For each relevant dimension, provide:

- Risk level: Low, Medium, High, or Not Assessable
- Signal: what in the artifact supports the judgment
- Implication: why it matters

Diagnostic dimensions:

- Confirmation bias
- Reactive opposition: overcorrecting against a disliked idea, source, institution, trend, person, or prior belief
- Missing context
- Too narrow
- Too sharply contextualized
- Recency bias
- Source selection quality
- Source diversity risk
- Assumption load
- Causality versus correlation
- Base-rate awareness
- Incentive awareness
- Counterargument quality
- Uncertainty handling
- Operational clarity
- Rhetorical pressure: urgency, fear, status pressure, social proof, identity cues, moral coercion, or false dichotomies

## Explorative Sources

After the cognitive diagnostic and before alternative hypotheses, recommend sources the user should consult to broaden perspective and keep their own biases in check.

Use this section when source diversity risk, missing context, reactive opposition, confirmation bias, or high stakes make additional voices especially valuable. In adaptive reports, include a short version when it would materially improve the user's next move.

Do not treat this as a generic bibliography. Recommend source categories, voices, evidence streams, or concrete source types that would expose the user to perspectives not already represented in the artifact.

Use this table:

| Source Direction | Why It Broadens the View | What To Look For |
| --- | --- | --- |
| Person, stakeholder group, discipline, institution, document type, dataset, or evidence stream. | Bias, blind spot, assumption, or missing context it helps correct. | Questions, claims, evidence, disagreement, or lived experience to seek. |

Strong explorative source directions often include:

- Primary stakeholders affected by the artifact's recommendation or framing
- Serious critics of the artifact's position
- Practitioners who live with the operational consequences
- Domain experts from adjacent disciplines
- Primary documents, policies, contracts, standards, or data
- Historical analogues that complicate the artifact's analogy
- International, cultural, class, gender, or minority perspectives when relevant
- Sources with different incentives from the artifact's author or cited authorities

## Alternative Hypotheses

Generate 2-4 plausible rival explanations, interpretations, or framings for the artifact's main conclusion when alternatives would improve the assessment.

Use this table:

| Alternative Hypothesis | What It Explains | What Would Support It | What Would Weaken It |
| --- | --- | --- | --- |

Do not create fake symmetry when the evidence strongly favors one view. Explain why a rival is weaker when appropriate.

## Assumption Ledger

List assumptions that materially affect trust in the artifact.

Use this table:

| Assumption | Type | Why It Matters | Confidence | How To Test |
| --- | --- | --- | --- | --- |
| Explicit or implicit assumption. | Factual, causal, value, scope, behavioral, strategic, or operational. | Impact on the argument or decision. | Low, Medium, or High. | Practical validation step. |

Prioritize assumptions that are load-bearing, fragile, hidden, or likely to change the user's decision.

## Calibration and Upgrade Plan

State the overall confidence level and main sources of uncertainty.

End with a prioritized upgrade plan:

1. Critical fixes: changes required before relying on the artifact.
2. Strengthening moves: additions that would materially improve trust.
3. Optional refinements: clarity, framing, structure, tone, or nuance improvements.
4. Thinking upgrades: 1-3 reusable cognitive moves the user can apply next time.

Include replacement language for weak claims when useful.

## Tone

Be rigorous without being theatrical. Flag problems clearly, but distinguish fatal defects, meaningful uncertainty, normal incompleteness, and easy-to-fix weaknesses.

When reviewing a user-produced artifact, be direct but developmental. When reviewing an artifact the user received, be direct about external risk without amplifying cynicism.

Help the user feel more capable, not merely judged.
