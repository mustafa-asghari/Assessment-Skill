# Custom Humanizer Pattern Bank

This is the assessment skill's own authenticity pattern bank. Do not copy an external humanizer list into this file. Add new patterns only when they are useful, source-backed, and relevant to assessment writing.

## How to Use

Treat these as review signals, not proof of misconduct. A pattern is a reason to inspect and improve the text. It is not evidence that a student cheated.

Fix patterns only when the fix preserves:

- The assessment meaning.
- The user's real work and voice.
- The official template structure.
- Citation and evidence accuracy.
- The selected `AiTone`.

## Current Source-Backed Signals

### Low variability and machine consistency

Research comparing human and LLM text finds that human writing often has more variability across linguistic features, while LLM writing can look unusually regular.

Check for:

- Paragraphs with nearly identical length.
- Repeated sentence shape across sections.
- Smooth but bland transitions at every paragraph boundary.
- Rubric answers that feel assembled from the same mold.

Improve by varying rhythm only where it helps readability. Do not add random errors.

Sources:

- Zanotto and Aroyehun, "Human Variability vs. Machine Consistency", 2024: https://arxiv.org/abs/2412.03025
- Georgiou, "Differentiating Between Human-Written and AI-Generated Texts", 2025: https://www.mdpi.com/2078-2489/16/11/979

### Dense formal academic register without student presence

LLM-assisted academic writing often leans toward dense nouns, nominalization, formulaic academic phrasing, and standardized formality.

Check for:

- Too many abstract nouns where a verb would be clearer.
- Repeated phrases like "effective implementation", "strategic approach", "comprehensive understanding", or "critical importance" without concrete detail.
- Reflection tasks with no real decision, uncertainty, mistake, limitation, or learning.
- Work that sounds more like a policy document than a student assessment.

Improve by adding accurate task-specific actions, evidence, constraints, or reflection from the user's context.

Sources:

- Georgiou, 2025: https://www.mdpi.com/2078-2489/16/11/979
- Cheng et al., "Writing without borders", 2025: https://www.nature.com/articles/s41599-025-05484-6

### Positive or polished sentiment that does not match the evidence

Post-ChatGPT student writing studies report shifts toward more formal and positive language without matching improvement in assessed quality.

Check for:

- Upbeat conclusions when the result was mixed.
- "Successful", "valuable", "effective", or "strong" claims with no evidence.
- Reflection that avoids mistakes, limits, or tradeoffs.
- Risk sections that sound reassuring rather than specific.

Improve by aligning tone with the evidence. If something failed, say so and explain the fix.

Source:

- Style, sentiment, and quality of undergraduate writing in the AI era, 2025: https://www.sciencedirect.com/science/article/pii/S2666920X2500147X

### Formulaic assessment structure

AI-generated university work can show formulaic structure, fragmented argument flow, excessive objectivity, and generic section logic.

Check for:

- Every section using the same mini essay format.
- Introductions that restate the question rather than begin the answer.
- Conclusions that summarize obvious points without adding assessment value.
- Lists of concepts that do not connect to the evidence.

Improve by following the rubric order, using evidence, and connecting each paragraph to the required competency.

Source:

- Nowacki and Wrochna, "ChatGPT theses", 2025: https://doi.org/10.1177/20427530251331083

### Low unpredictability and over-clean surface

Detector research often uses perplexity, lexical variation, stop-word patterns, discourse markers, subjectivity, readability, grammar errors, and quote counts. AI text can be more predictable, cleaner, and less varied.

Check for:

- Perfectly clean prose that lacks the user's actual context.
- No quotations or concrete source references in research-heavy work.
- Repeated discourse markers such as "furthermore", "moreover", "therefore", and "in conclusion".
- Title or task phrase repeated too often.

Improve by adding real source detail, user-specific context, and direct wording where appropriate. Do not add fake mistakes.

Source:

- Mindner et al., "Classification of human- and AI-generated texts for different languages and domains", 2024: https://link.springer.com/article/10.1007/s10772-024-10143-3

### Detector-score overconfidence

Commercial and institutional guidance warns that detector scores can be wrong and should not be used alone.

Check for:

- Claims that a detector "proves" text is human or AI.
- Attempts to write for a detector instead of writing for the assessment.
- Ignoring drafts, evidence, version history, or source files.

Improve by prioritizing real process evidence, truthful citations, version history, screenshots, and assessor-readable explanations.

Sources:

- Turnitin AI Writing Report guide, updated 2026: https://guides.turnitin.com/hc/en-us/articles/22774058814093-Using-the-AI-Writing-Report
- OpenAI AI classifier note, 2023: https://openai.com/blog/new-ai-classifier-for-indicating-ai-written-text
- RAID benchmark, 2024: https://arxiv.org/abs/2405.07940

### Weak provenance or recreated evidence

Evidence should come from the real app, file, terminal, browser, document, or tool. Recreated images are weak unless clearly labeled.

Check for:

- Screenshots that do not show the relevant tool, file, timestamp, output, or context.
- Diagrams or images that look newly generated when the task asked for evidence of work.
- Missing file paths, app names, command output, or version history.

Improve by capturing real evidence from the source app/tool after user permission.

Sources:

- C2PA specification: https://spec.c2pa.org/specifications/specifications/1.4/specs/C2PA_Specification.html
- SynthID-Text Nature paper, 2024: https://www.nature.com/articles/s41586-024-08025-4

## Add-New-Pattern Gate

Before adding a pattern:

1. Verify it from a primary source, peer-reviewed paper, official platform documentation, or reputable institutional guidance.
2. Write the pattern as a review signal, not as a detector-bypass trick.
3. State how to improve honestly.
4. Add a dated entry to `research-ledger.md`.
5. Keep examples short and original.
