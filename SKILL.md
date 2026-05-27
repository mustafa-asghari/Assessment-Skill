---
name: assessment-skill
description: Complete assessment tasks with rigorous intake, planning, evidence collection, template preservation, multi-agent chunking, evaluator and strict teacher review, and a bundled source-backed humanizer. Use when Codex, Claude, opencode, or another agent is asked to understand an assessment brief, attached files, rubric, marking criteria, official template, screenshots/evidence requirements, or final submission package.
---

# Assessment Skill

Use this skill to complete an assessment accurately, honestly, and in the required format. The main agent owns the whole assessment. Subagents may draft, research, collect evidence, or review chunks, but the main agent remains responsible for correctness, template preservation, evidence quality, and final teacher review.

Do not copy or depend on an external humanizer skill. This skill has its own authenticity editor in `references/humanizer/`.

## Start Rules

1. Read the assessment brief, rubric, marking criteria, attached files, official templates, examples, required evidence, and local project context before drafting.
2. Create a persistent goal for the full assessment where the runtime supports it.
   - Codex: use `/goal` or the goal tool if available.
   - Claude: use `/goal` if available.
   - Other agents: state the full objective in working memory and continue until the complete workflow is done.
   - Do not mark the goal complete until the strict teacher review passes.
3. Load the selected tone file from `references/AiTone/` after asking the user to choose `formal`, `friendly`, or `informal`.
4. Load `references/humanizer/rewrite-protocol.md` before editing assessment prose.
5. Load `references/humanizer/pattern-bank.md` before evaluator or teacher checks for AI-like writing.
6. Ask all blocking questions near the start. Do not keep interrupting later unless a new issue blocks correctness.
7. Never invent assessment facts, fake evidence, fake citations, fake screenshots, fake tool output, or fake personal experience.

## Intake Checklist

Build an assessment plan before execution. Capture:

- Task title, course/unit, due date, audience, deliverables, submission format, and word/page limits.
- Rubric criteria, satisfactory/unsatisfactory rules, required competencies, and any "must include" items.
- Official templates, locked structure, fillable sections, required naming, and formatting rules.
- Whether AI assistance is allowed, limited, or prohibited by the assessment rules.
- Required screenshots, source files, logs, terminal output, LMS evidence, browser evidence, documents, spreadsheets, slides, diagrams, or citations.
- User tone choice and any writing sample, preferred voice, personal context, workplace context, or project details needed to answer honestly.
- Tools, skills, apps, browser targets, local files, and permissions needed.

If any high-impact item is missing, ask the user before drafting. Good initial questions usually cover tone, missing personal details, missing files, evidence permissions, citation style, and whether the user has an official template.

## Tool and App Planning

Plan tools before doing assessment work.

- Inspect relevant local files and installed apps when evidence depends on real software or user work.
- Choose the best real source app/tool for evidence. Do not recreate evidence in a new image or mockup when a real app, file, terminal, browser page, document, spreadsheet, or existing screenshot can be used.
- Ask permission before controlling the user's computer, opening private apps, navigating accounts, or taking screenshots.
- For coding evidence, choose based on OS, language, framework, and installed apps. Examples: Rider is often suitable for C# on macOS; Visual Studio or VS Code may be better on Windows; Xcode is suitable for iOS/macOS projects; Android Studio is suitable for Android projects.
- Use browser evidence only for web apps, LMS pages, online tools, research sources, or assessment instructions that require a browser.
- If no real source exists, ask the user whether to proceed with a recreated illustrative asset. Label any generated or recreated asset honestly.

## Template Rules

Official templates are locked.

- Do not change, move, rename, reorder, delete, replace, restyle, or redesign template headings, tables, fields, numbering, placeholders, or layout.
- Fill only the required sections.
- Preserve empty optional sections unless the assessment instructs otherwise.
- If the template appears broken, duplicated, or contradictory, ask the user before changing structure.
- If no template exists, choose a clear human assessment structure that follows the rubric and task order.

## Multi-Agent Workflow

Use native delegation where available. In Codex, use subagents only when the user or skill request authorizes agent delegation, and assign bounded work with clear ownership.

1. Split the assessment by rubric criterion, task part, evidence group, or template section.
2. Give each subagent a compact brief:
   - Assessment objective and selected tone.
   - Assigned chunk and exact boundaries.
   - Relevant rubric criteria.
   - Template rules.
   - Evidence files/paths/screenshots it may use.
   - Humanizer rewrite rules relevant to the chunk.
   - Prohibition on fabricating evidence, citations, or personal claims.
3. The main agent reviews each chunk before integration.
4. If chunks conflict, the main agent resolves them against the brief and rubric, not by averaging outputs.

## Evaluator Pass

After each chunk:

- Check that the answer directly addresses the assigned task.
- Check rubric coverage and satisfactory evidence.
- Check that official template structure is untouched.
- Check citations, screenshots, code output, logs, or other evidence against the source.
- Check tone against the chosen `AiTone` file.
- Run the custom humanizer protocol for AI-like patterns.
- Send concrete feedback back to the subagent. Require fixes before integration.

## Agent Renewal

Retire a subagent when performance degrades.

Signals include repeated missed feedback, drift from the rubric, stale context, contradictions, fabricated details, ignoring template rules, slowing output, or quality dropping after a long thread.

When renewal is needed:

1. Close or stop using the weak subagent.
2. Spawn a new subagent if the runtime supports it.
3. Give the replacement a compact dossier:
   - Current assessment goal.
   - User answers and selected tone.
   - Files/templates/rubric used.
   - Completed work and accepted chunks.
   - Current chunk.
   - Failed checks and feedback history.
   - Evidence paths and screenshots.
   - Humanizer rules already applied.
4. Do not ask the new subagent to reread irrelevant history.

## Teacher Review

The teacher agent is strict. It acts like a marker trying to decide whether the submission is satisfactory.

Teacher review must check:

- Every rubric item and task instruction.
- Template preservation.
- Evidence authenticity and relevance.
- Citation accuracy and source fit.
- Missing assumptions, unsupported claims, hallucinated facts, or unverifiable personal details.
- AI-like writing patterns using `references/humanizer/pattern-bank.md`.

If the assessment is too large for one teacher context, split review across specialist teacher agents by section, rubric area, evidence type, or template part. Merge findings before deciding pass/fail.

The teacher should perform fresh web research for current AI-writing patterns, detector limitations, and platform behavior when the assessment has high AI-authenticity risk or when new patterns are suspected. Use primary sources, academic papers, official detector/platform documentation, or reputable institutional guidance where possible.

If the teacher finds a valid source-backed pattern missing from `references/humanizer/pattern-bank.md`, update `references/humanizer/research-ledger.md` and add the pattern to the bank if the skill directory is writable. If the skill cannot be edited, add it to the assessment notes and report it in the final response.

Even if the rubric passes, fix avoidable AI-like text found by the teacher unless the fix would break template structure, meaning, evidence, citation accuracy, or the user's permitted voice.

## Final Packaging

Before final delivery:

- Confirm the `/goal` remains open until teacher review passes.
- Recheck template structure and required file names.
- Verify evidence files exist and are referenced correctly.
- Confirm no generated/recreated evidence is presented as real evidence.
- Confirm all citations are real and attached to claims they support.
- Confirm the selected tone is consistent.
- Summarize what was completed, what evidence was used, and any remaining user action required for submission.

Only mark the goal complete after the teacher review passes and the final deliverable is ready.
