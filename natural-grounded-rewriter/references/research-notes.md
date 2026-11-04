## 20. Evidence traceability and research limits

The complete workflow is an editorial design proposal, not a research-validated detector or intervention. Only the associations mapped below should carry a research-association label without additional documentation. Other diagnostic entries are editorial concerns or weak surface clues.

| Pattern or principle | Supporting source and setting | Observed finding | Limitation and editing consequence |
|---|---|---|---|
| Nominalization, participial clauses, phrasal coordination, subject that-clauses | [Reinhart et al.](https://pmc.ncbi.nlm.nih.gov/articles/PMC11874169/), comparisons of English human text and GPT-4o/Llama variants | Some instruction-tuned models favored these grammatical forms. | Model and genre dependent; inspect function and concentration, not individual occurrences. No automatic deletion rule. |
| Vocabulary clues, formulaic organization, vague conclusions, repetitive quotation presentation | [Russell et al.](https://aclanthology.org/2025.acl-long.267/), experienced readers assessing generated and human nonfiction articles | Readers used lexical and higher-level clues; some clues also produced mistakes. | A reader's explanation is not proof of a universal causal signal. Revise only when a reader-facing defect exists. |
| Lexical and syntactic variability | [Bagdasarov and Alves](https://aclanthology.org/2025.lm4dh-1.4/), scientific human and model-generated texts | Human texts showed more syntactic variability; generated texts more lexical variability in the sample. | Do not assume greater vocabulary diversity always means more human writing. No diversity quota. |
| Changing lexical associations | [Geng and Trotta](https://aclanthology.org/2025.findings-acl.657/), academic abstracts over time | Frequencies of some words associated with ChatGPT changed after public attention. | Population trends cannot establish individual authorship; avoid permanent word blacklists. |
| Prompt-conditioned language patterns | [Prompt sensitivity study](https://onlinelibrary.wiley.com/doi/10.1111/modl.70089), corpus-based analysis of generated language | Linguistic comparisons can depend on generation prompts. | Document prompt conditions when evaluating; do not generalize one sample into universal grammar rules. |
| Detector generalization limits | [RAID](https://aclanthology.org/2024.acl-long.674/), varied models, domains, and generation/modification conditions | Detection performance changed across conditions. | Detector scores are not editorial success metrics. |

Detector background only: [DetectGPT](https://proceedings.mlr.press/v202/mitchell23a.html) studies probability perturbation; [Binoculars](https://proceedings.mlr.press/v235/hans24a.html) contrasts model scores; [SynthID-Text](https://www.nature.com/articles/s41586-024-08025-4) concerns deliberate statistical watermarking. These sources do not justify manipulating prose to chase a presumed detection threshold.

Before adding a research label, record the source, date, language, genre, models or participants, observed association, limitations, and whether it supports any editing decision. Keep association separate from a proposed repair: a study documenting a pattern does not prove that removing it improves writing.

The previous research discussion centered mainly on English. Apply the explicit language rules in Section 7, and evaluate other languages with appropriate material and reviewers. Do not claim multilingual performance based only on English tests.

### Research verification record

Last bibliography/access check: 4 November 2026. This is a source-record and relevance check, not replication of experiments or a new systematic literature review.

- Russell et al., Bagdasarov and Alves, Geng and Trotta, and RAID: ACL Anthology records accessible; titles/authorship and the recorded research setting remain traceable to the linked records.
- Prompt sensitivity: Wiley record accessible; title, authors Peter Crosthwaite, Shuyi (Amelia) Sun, and Feng (Kevin) Jiang, and first-publication date 20 August 2026 confirmed. The abstract addresses prompt specificity in metadiscourse comparisons.
- Reinhart et al.: the PMC URL returned a browser challenge on this check. The [author preprint record](https://arxiv.org/abs/2410.16107) was accessible and confirmed the title/authors; it lists a revised preprint version dated 21 August 2025. Do not conflate that revision date with the journal publication date. The earlier journal-based association remains recorded; a fresh journal full-text verification was not completed in this pass.
- DetectGPT and Binoculars: PMLR records accessible; titles, author lists, publication years, and abstract-level mechanisms confirmed.
- SynthID-Text: the Nature URL encountered an access redirect in this pass. Retained from the earlier source review; not claimed freshly full-text verified.

Record verification date, authoritative URL, bibliographic identity, relevant finding, and access limits when updating an association. Recheck affected sources when changing research claims, before a major release, or when a broken link, correction, or newer evidence warrants review. Do not silently infer that an inaccessible paper is invalid or that access success proves its findings universally apply.
