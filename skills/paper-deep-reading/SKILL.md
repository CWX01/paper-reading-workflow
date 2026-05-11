---
name: paper-deep-reading
description: Deep-read academic papers and produce structured Chinese research notes with critical analysis.
---

# Paper Deep Reading

## Overview

Use this skill to turn a paper into a durable Chinese research note, not a loose summary. Prioritize factual grounding, explicit uncertainty, and connections to the user's existing paper-reading repository.

This skill handles both research papers and review articles (综述). The workflow below applies to both; review-specific branches are noted at each step where they differ. Always determine the paper type before starting.

For the full note schema, read `references/note-schema.md` (or `references/review-article-note-schema.md` for review articles) when creating or revising a note file.

## Workflow

1. Resolve the paper source.
   - If the user gives a local PDF or md, read it directly.
   - If the user gives a URL, open or download the paper from that URL.
   - If the user gives only a title, search for an official source first: arXiv, publisher page, author page, DOI, conference page, or project page.
   - When working inside a paper-reading repo, search `README.md`, `notes/`, `papers/`, and `literature/` for existing notes or local copies before creating a new note.
   - Record the source URL and access path in the note.
   - If metadata is uncertain, mark it as `Unknown` or `TBD`; do not invent venue, year, code, dataset, or claims.

2. Extract core metadata.
   - Title, authors, venue, year, paper link, code link, dataset link, artifact link, scope/subfield, topic tags, and reading status.

3. Read in three passes.
   - Pass 1: Abstract, introduction, conclusion. Identify the problem, essential motivation, basic idea, claimed contributions, and main result. Do not stop at surface motivation; distinguish the real pain point, missing capability, broken assumption, or research gap that makes the paper worth doing.
   - Pass 2: Method, assumptions, algorithms, system design, and definitions. Extract the paper's actual mechanism instead of paraphrasing only at a high level. Reconstruct how the basic idea could be derived from the motivation and then developed into the concrete method.
   - Pass 3: Evaluation, tables, figures, ablations, case studies, limitations, and related work. Check whether the experiments support the claims.
   - For review articles, adapt the passes:
     - Pass 1: Abstract, introduction, conclusion. Identify the review's scope, organizational logic (taxonomy, timeline, or problem decomposition), main conclusions, and the gap it fills.
     - Pass 2: Skim the full structure to understand the section layout and identify which chapters cover principles/methods (detailed) vs. applications/cases (brief). Read each section following the body section checklist in the review schema.
     - Pass 3: Cross-section synthesis. Identify cross-chapter findings, trends, and open questions. Inventory key comparison tables (full content) and important figure titles.

4. Extract evidence artifacts.
   - Inventory the paper's central figures, tables, equations, algorithms, and definitions.
   - Include the artifacts that carry the paper's main claims; if the user asks for exhaustive notes, include every figure, table, and important equation.
   - For formulas and algorithms, preserve the paper's notation and check for variable meaning, ranges, missing operators, and consistency with the surrounding text.
   - For tables and figures, state what each one is evidence for instead of only describing its appearance.
   - For review articles: record key comparison tables in full (taxonomy tables, method summary tables, benchmark comparison tables). Record important figure titles only; the user will consult the original for details.

5. Position against prior work.
   - Identify the closest prior work and the paper's claimed delta.
   - Distinguish method novelty, setting novelty, data novelty, and finding novelty.
   - If the delta depends on recent work or post-publication impact, search current sources and cite them.
   - For review articles: this step is less critical since the review itself positions prior work. Focus on noting the review's organizational framework and any explicit comparisons to earlier surveys in the same area.

6. Run a critical synthesis pass.
   - Ask whether the work is convincing, useful, reproducible, and well-scoped.
   - Check the core questions: what problem is being solved, what prior practice failed to handle, what is new, who benefits, what can go wrong, what it costs to reproduce or deploy, and whether the experiments actually test the claim.
   - Check whether the method really follows from the stated motivation, or whether the motivation is mostly post-hoc framing.
   - For review articles, check: Is the scope well-defined and justified? Is the taxonomy/framework useful and non-trivial? Are important sub-directions or works missing? Is the coverage current? Are the comparison tables fair and complete? Does the review offer genuine synthesis or just a paper-by-paper summary?
   - Use this as an internal analysis pass. Do not create a separate critical-review section in the final note.
   - Convert the judgment into the final note's `Strengths`, `Limitations`, and `My Takeaways` sections.
   - Keep attribution clear in prose when needed: separate what the paper demonstrates from what the reader concludes.
   - Make critique concrete: reproducibility, cost, etc.
   - If evaluating post-publication impact, adoption, or follow-up work, search the web in the same turn and cite the sources used. Do not cite impact from memory.

7. Write the note in Chinese.
   - Use the schema in `references/note-schema.md` (or `references/review-article-note-schema.md` for review articles).
   - Keep paper terms precise; preserve key English terms in parentheses when translation may lose meaning.
   - Separate the authors' claims from your analysis.
   - After `TL;DR`, add a short `毒舌评论`: one sharp paragraph or 2-3 bullets that gives a hard, fact-grounded judgment on the paper's real value, biggest weakness, possible overclaim, or most fragile assumption. It must not be a summary. Make the verdict sting, but do not invent defects or state uncertain criticisms as facts.
   - For research papers:
     - Give special attention to `Motivation and Basic Idea`: explain the most fundamental reason the paper exists and the simplest idea the method is built on.
     - Keep `Background` concise: record only the chain from background to problem to gap. Do not write a long textbook-style background section.
     - In `Method`, analyze how the basic idea becomes the concrete method. Ground this in the paper's text, related work, assumptions, ablations, or system constraints; if the logic is inferred, label it as inference.
     - Keep `Evaluation` focused on experiment idea, evaluation metrics, and results. Include dataset scale, baselines, or key figures only when they are necessary to understand the result.
   - For review articles:
     - In `Motivation and Basic Idea`, focus on the review's logic and how it structures the field.
     - The body sections should follow the review's own section structure using original section numbers. Use the body section checklist in the review schema. Adjust detail level by section type: principles and methods get detailed treatment, applications and cases get brief summaries.
     - Do not record individual cited papers; the user will consult the original when needed.
     - Record key comparison tables in full. Record figure titles only.
     - In `Findings`, only record cross-section conclusions with section numbers (e.g., §3.2).
   - End with connections to prior/future papers and questions worth revisiting.

## Output Files

When the user wants notes saved in the current repo:

- Use filenames like `0Report_<paper-short-title>.md`, such as `0Report_attention is all you need.md`.
- Prefer editing an existing note over creating duplicates for the same paper.

## Quality Bar

- Do not rely on abstract-only summaries unless the paper cannot be accessed; state that limitation clearly.
- The `毒舌评论` must be meaningfully sharper than the TL;DR. If it could be mistaken for a neutral summary, rewrite it.
- Do not overclaim novelty; describe novelty as the paper frames it and compare to related work when available.
- Do not omit assumptions. 
- Preserve equations, algorithms, and important definitions when they are essential to the paper.
- Preserve the evidence trail: key figures, tables, datasets, metrics, and ablations should be traceable to the claims they support.
- Prefer specific critique.

For review articles, additionally:
- Body sections must use the review's original section numbers and follow its structure; do not reorganize into a fixed template.
- Key comparison tables (taxonomy, method summary, benchmark) must be recorded in full, as they are the core value of a review.
- `Findings` must cite specific section numbers (e.g., §3.2) for traceability.
