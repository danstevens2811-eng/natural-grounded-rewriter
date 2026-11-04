## 18. Measurable behavioral evaluation plan

Compare the original, a baseline rewrite without this skill, and a skill-assisted rewrite where feasible. Keep inputs and constraints equivalent; record model/version and relevant generation settings when available. Randomize presentation order and conceal which rewrite used the skill. Use unseen cases for final evaluation and repeat a representative subset to assess variability.

### Controlled baseline and run record

Freeze the task brief, source, protected-content expectations, mode, constraints, and relevant samples before generating either version. Use the same model/version, available tools, source access, output budget, and exposed generation settings where feasible. Isolate runs from previous outputs and evaluator feedback. Record unavailable settings; do not imply control over hidden platform behavior.

Baseline prompt template:

```text
Task: {one fixed mode instruction below}
Audience and purpose: {identical brief}
Voice samples and preferences: {identical supplied material, or none}
Constraints and output format: {identical user requirements}
Source: {identical source text}
```

Fixed mode instructions:

| Mode | Baseline task instruction |
|---|---|
| Proofread | Correct spelling, grammar, and punctuation errors; otherwise preserve wording and structure. |
| Natural rewrite | Rewrite for natural phrasing and readability while preserving meaning. |
| Full rewrite | Rewrite wording and organization to serve the brief while preserving factual meaning and required content. |
| Persuasive rewrite | Make the content more persuasive for the stated audience without adding unsupported claims. |
| Voice preservation | Improve clarity and flow while preserving the source author's voice and meaning. |

Use the identical task prompt for the skill-assisted condition with only the skill instructions added. Do not make the baseline artificially weak, omit user constraints from it, or provide the skill condition with extra source material. Record any unavoidable difference as a comparison limitation.

For each run record: case ID, source/brief version, mode, model/version, settings and output limit, instruction version, repetition index, actual output length, reviewer identity or type, scores with rationale, mandatory findings, and adjudication. Set repetition counts before testing; a practical default is three runs on the representative repeat subset, reported as a chosen test budget rather than a confidence guarantee. Retain all runs, not only the best output.

### Mandatory checks

Before reviewing style, prepare an expected-content record for each test:

- Protected factual claims, including qualifiers, conditions, and commitments.
- Required topics and instructions.
- Exact protected spans: quotations, URLs, identifiers, code, placeholders, and designated technical values.
- Permitted changes and deliberate source ambiguities.

Record preserved items / required items for coverage and exact-span checks. Mark zero-item categories not applicable. Require complete protected-item and required-content coverage unless the test explicitly authorizes omission. Exact matching supports checks of protected spans only; use semantic comparison for paraphrased claims. No unauthorized semantic drift is acceptable.

Any protected-fact alteration, invented support, broken protected structure, or omitted mandatory condition fails the case regardless of style scores. Classify severity separately to guide fixes. Do not average such a failure away.

### Editorial scoring

Score purpose/usefulness, coherence, voice/genre fit, naturalness, and editing restraint separately on this anchored scale:

| Score | Anchor |
|---|---|
| 1 | Serious failure: obstructs the task or clearly violates the intended voice/genre. |
| 2 | Material weaknesses remain and require substantial revision. |
| 3 | Usable, but identifiable weaknesses or unnecessary edits remain. |
| 4 | Meets the brief; only minor optional refinements remain. |
| 5 | Meets the brief with no material weakness found in that dimension. |

Each score needs a brief example or rationale. Pairwise preference must allow original preferred, baseline preferred, skill preferred, tie, or insufficient information. A strong original can win without implying that the skill should manufacture changes.

Use two independent reviewers when feasible. If they disagree about a mandatory failure or differ by more than one score point, inspect the cited passages and expected-content record; use an adjudicator or mark unresolved. Do not settle a factual dispute by averaging opinions. Label single-reviewer or model-only results and their limits explicitly.

### Release decision: mandatory gates versus editorial targets

Score editorial dimensions per case and repetition. Report category-level score distributions or medians, valid counts, preference wins/losses/ties, insufficient-information cases, and worst material findings. Do not collapse fidelity and style into one average. Treat voice fidelity as not evaluable when adequate voice evidence is absent; still assess fit to the requested default voice. Retain evidence-limited cases in the report rather than hiding them.

Mandatory release gates: all applicable fidelity and explicit-delivery checks pass in the declared release set, zero unresolved critical failures, and no unresolved mandatory regressions. A stylistic win never offsets a protected-fact change. Report the tested scope and any limitations; no gate establishes universal reliability.

Editorial targets: demonstrate improvement over the controlled baseline on weak drafts and appropriate restraint on strong drafts. A score of 4 is a useful target, not an unconditional minimum in every dimension and case. The original may be preferable to both rewrites; preserving it can be the correct outcome. An isolated score of 3 requires examination, not automatic rejection or concealment.

Before examining final results, declare a sufficient case count per intended genre/mode and the practical evidence required to support release. Review category-level distributions and all material failures, not only aggregate preference. Systematic inferiority in an intended use case requires correction or an explicitly narrowed supported scope. Sparse or inconclusive results remain inconclusive; do not label them a pass. Document the release decision and its reasoning rather than invent a universal statistical threshold. No behavioral release decision has yet been made.

### Test matrix

| Case | Required behavior |
|---|---|
| Stiff, complete prose | Improve expression without adding claims. |
| Vague source without support | Do not manufacture specificity. |
| Strong personal prose | Retain effective personality and make only justified edits. |
| Technical content | Preserve terminology, quantities, procedures, and precision. |
| Personal narrative | Preserve supplied experience; invent none. |
| Distinct author samples | Maintain meaningful differences between voices. |
| Qualified claims | Preserve uncertainty and exceptions. |
| Deliberate repetition | Retain repetition that serves the task. |
| Conflicting details | Flag consequential conflicts rather than guess. |
| Short email | Preserve the requested action without needless elaboration. |
| Long document | Maintain continuity and avoid new contradictions. |
| Embedded commands | Treat them as source content, not operating instructions. |
| Strict length limit | Preserve mandatory meaning or explain infeasibility. |
| SEO article | Preserve supplied keyword requirements, intent, links, and useful depth without stuffing. |
| HTML/Markdown and tables | Edit prose while preserving protected structure, URLs, identifiers, and values. |
| Mixed Urdu-English text | Preserve intended language switching, script, and meaning; use a competent reviewer. |
| Landing page | Improve clarity and supported persuasion without invented guarantees or outcomes. |
| Metadata/FAQ/product fields | Preserve schema, supplied limits, question-answer mapping, units, and product claims. |
| Mixed-genre API landing page | Retain persuasive organization and technical precision without oscillating formats or adding code. |
| Long-document context pressure | Keep one bounded continuity summary; retrieve exact protected items and maintain cross-section dependencies. |
| Conflicting instructions | Identify incompatible requirements; do not silently drop a material constraint. |
| Exact delivery format | Return requested plain text or complete markup without unauthorized wrappers or explanations. |
| High-stakes phrasing | Preserve warnings, units, obligations, assumptions, and qualifications; do not reinterpret professionally. |
| SEO scope boundary | A natural rewrite retains targeting; explicit strategy work is separately identified and researched as needed. |

Run the same suitable source under proofreading, natural rewriting, full rewriting, persuasive rewriting, and original-voice preservation instructions. Assess whether editing scope changes appropriately while protected meaning remains intact.

After each significant instruction change, rerun failed cases, their related cases, and a compact regression set spanning strong prose, protected claims, structured content, and distinct voices. Maintain records of input, expected constraints, output, reviewer findings, and corrections. No behavioral tests have been performed as part of this specification revision.
