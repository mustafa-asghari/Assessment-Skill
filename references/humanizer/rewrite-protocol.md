# Rewrite Protocol

Use this protocol when revising assessment prose for authenticity, clarity, and marking quality.

## Non-Negotiables

- Do not fabricate claims, citations, screenshots, results, workplace experience, or personal reflection.
- Do not alter official template structure.
- Do not remove required rubric wording if the assessment expects it.
- Do not optimize for detector evasion. Optimize for honest, specific, assessor-readable work.
- Do not add deliberate spelling or grammar errors.

## Inputs

Before rewriting, collect:

- The selected tone file from `references/AiTone/`.
- The task instruction and rubric criterion.
- Any official template constraints.
- The user's real details, evidence, source files, screenshots, logs, or citations.
- The current draft.
- Relevant patterns from `pattern-bank.md`.

## Rewrite Steps

1. Mark the assessment purpose of the passage.
2. Identify unsupported claims, generic statements, missing evidence, and AI-like patterns.
3. Replace vague claims with real task evidence or ask the user if the detail is missing.
4. Keep the user's meaning and required competency language.
5. Adjust tone using the selected `AiTone` file.
6. Vary rhythm where the text reads too uniform, but do not add forced personality.
7. Re-check citations and evidence references.
8. Re-check template structure.
9. Run a final authenticity audit:
   - What sounds assembled, over-polished, generic, too positive, or unsupported?
   - What would a strict marker question?
   - What evidence would make this more credible?
10. Apply fixes and pass the section back to the evaluator.

## Reflection Writing

For reflective assessment tasks:

- Include real action, choice, result, and learning.
- Mention uncertainty or limitation when true.
- Avoid perfect growth-story endings.
- Prefer concrete workplace or project details over broad claims.

Weak: "This experience enhanced my communication skills and highlighted the importance of teamwork."

Better: "I had to slow the discussion down because two team members were talking past each other. I summarised the issue on the whiteboard, then asked each person what outcome they needed before we chose the next step."

## Research Writing

For research-based assessment tasks:

- Tie every source to a claim.
- Avoid vague source phrases such as "studies show" unless the study is named or cited.
- Summarise sources accurately. Do not cite a source for a claim it does not make.
- Use current sources when the topic changes over time.

## Evidence Writing

For screenshot, coding, system, or workplace evidence:

- Say what the evidence shows.
- Reference the real app/tool/file/path where useful.
- Explain why it satisfies the criterion.
- Do not create a clean-looking substitute when real evidence is available.

## Output for Subagents

When returning a rewritten chunk, include:

- Revised text.
- Evidence/citation notes.
- Any unresolved questions.
- Any template constraints preserved.
- Humanizer patterns fixed.
