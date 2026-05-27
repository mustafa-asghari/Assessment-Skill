# Assessment Skill

This skill helps an AI agent complete assessment tasks from the brief, rubric, attached files, templates, and required evidence. It is designed for Codex, Claude, opencode, and similar coding agents.

The skill includes:

- Assessment intake and planning.
- `/goal` setup for Codex and Claude where supported.
- Tone selection: formal, friendly, or informal.
- Locked official-template handling.
- Local app and evidence discovery before screenshots.
- Multi-agent chunking, evaluator review, strict teacher review, and agent renewal.
- A bundled custom humanizer module backed by research notes.

## Files

- `SKILL.md` - main skill instructions.
- `references/AiTone/formal.md` - formal tone prompt.
- `references/AiTone/friendly.md` - friendly tone prompt.
- `references/AiTone/informal.md` - informal tone prompt.
- `references/humanizer/pattern-bank.md` - custom AI-pattern and authenticity checks.
- `references/humanizer/rewrite-protocol.md` - rewrite and review workflow.
- `references/humanizer/research-ledger.md` - dated source-backed pattern updates.
- `agents/openai.yaml` - Codex UI metadata.

## Repository

This skill is distributed from:

```text
git@github.com:mustafa-asghari/Assessment-Skill.git
```

The repository is meant to be used with `SKILL.md` at the repo root. Users can install the skill from GitHub or clone it into their local skills folder.

Recommended repo layout:

```text
assessment-skill/
├── SKILL.md
├── README.md
├── agents/
│   └── openai.yaml
└── references/
    ├── AiTone/
    └── humanizer/
```

The skill name comes from `SKILL.md`:

```yaml
name: assessment-skill
```

## Installing from GitHub

### Codex skill installer

If the user has Codex's skill installer available, they can ask their agent:

```text
Install the Codex skill from GitHub repo mustafa-asghari/Assessment-Skill at path .
```

If their agent accepts an SSH Git URL, they can use:

```text
Install the Codex skill from git@github.com:mustafa-asghari/Assessment-Skill.git
```

After installation, restart Codex so it picks up the new skill.

### Manual install

Users can also clone the repo directly into their skills folder:

```bash
mkdir -p ~/.codex/skills
git clone git@github.com:mustafa-asghari/Assessment-Skill.git ~/.codex/skills/assessment-skill
```

Then restart Codex and invoke:

```text
Use $assessment-skill for this assessment. The brief, rubric, and template are attached.
```

### Private repos

For a private repo, users need GitHub access through their existing git credentials, SSH key, or `GITHUB_TOKEN`/`GH_TOKEN`, depending on their agent's installer.

## How to use it after installation

### Option 1: Invoke by skill name

After installation, start a new agent chat and write:

```text
Use $assessment-skill to complete this assessment.

First read the assessment brief, rubric, templates, and attached files. Set /goal if supported. Ask me all required questions up front, including tone, missing details, and evidence permissions. Then split the work into chunks, use subagents where useful, run evaluator checks, run strict teacher review, and produce the final submission.
```

## What the agent should ask first

The skill is designed to ask all important questions at the start, usually:

- Which tone to use: formal, friendly, or informal.
- Whether there is an official template.
- Whether the agent has permission to open apps, browse pages, or take screenshots.
- Which evidence is real and where it lives.
- Any personal, workplace, or project details the assessment requires.
- Citation style and submission format if the brief does not specify them.

## Evidence and screenshots

The agent must use real evidence where possible. It should inspect relevant files and installed apps, then capture screenshots from the actual app, browser, terminal, document, spreadsheet, or tool.

It must not recreate, redraw, or generate evidence images unless no real source exists and you approve an illustrative substitute.

## Teacher and humanizer review

Before final delivery, the skill runs a strict teacher review against the rubric and marking criteria. It also checks the writing with the bundled humanizer module.

If the teacher finds a new source-backed AI-writing pattern during fresh research, the skill should update the humanizer research ledger and pattern bank when the skill folder is writable.

## Example prompt

```text
Use $assessment-skill to complete my assessment.

Files are in /path/to/assessment-folder.
Use the official template exactly as provided. Do not change the structure.
Ask me all questions first. Use a friendly tone unless the rubric requires formal writing.
Use real screenshots from the relevant apps only after asking permission.
Run the strict teacher review before giving me the final file.
```
