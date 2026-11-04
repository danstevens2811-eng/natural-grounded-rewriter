## 19. Independent evaluator brief

The following instructions apply when the user explicitly asks another model to evaluate this specification.

Evaluate the design independently. Do not assume it deserves 10/10 or that its claims have been behaviorally validated. Distinguish design quality from measured performance. Do not claim to have tested outputs unless you actually produced or inspected them.

Review for:

1. Contradictory or ambiguous instructions.
2. Missing safeguards against meaning drift or invented specificity.
3. Overediting and voice homogenization risks.
4. Unnecessary complexity, reference duplication, and context cost.
5. Unsupported assumptions about human writing or AI detection.
6. Genre, language, and audience limitations.
7. Inadequate stopping rules or evaluation coverage.
8. Whether another model could implement and follow the specification without further clarification.

For each material finding, report: section, severity, concrete failure scenario, and the smallest useful correction. Cite the relevant instruction rather than giving generic advice.

Rate these dimensions separately from 1 to 10:

- Scope and instruction clarity.
- Factual and semantic preservation.
- Voice and genre adaptability.
- Rewriting usefulness and restraint.
- Efficiency and maintainability.
- Evaluation quality and honesty about limitations.

Score anchors: 1–3 unusable or unsafe for its intended function; 4–6 substantial unresolved gaps; 7–8 sound design with material improvements needed; 9 strong design with minor gaps; 10 no material design gaps found within the stated scope. A design score of 10 does not establish perfect execution.

If reporting an overall score, disclose how it was calculated and list unresolved critical findings separately. Use “not evaluated” for behavioral performance when no test was run. End with an implement / revise before implementation / insufficient information recommendation.

Optional evaluation output format:

```text
Verdict:
Design scores:
Critical and material findings:
Concrete failure scenarios:
Proposed minimal revisions:
Tests performed and actual outcomes:
Untested uncertainties:
Implementation recommendation:
```
