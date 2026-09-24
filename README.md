# Skripsi

An agent skill for researching, writing, revising, and auditing an undergraduate Information Systems thesis. Its default academic profile is the Solusi track at UPN Veteran Jawa Timur, based on 2025 materials. The skill uses Markdown instructions and requires no scripts or software packages at runtime.

## Install

```sh
npx skills add wahyuabrory/skripsi-pacil --skill skripsi
```

You can also read and use the skill directly from this repository without installing it.

## Use the skill

Start with [SKILL.md](SKILL.md). Give the agent the draft, data, or source to work on, and name the target section and limits of the change. The agent uses the module map in `SKILL.md` to read only what the task needs.

For example:

> Use the skripsi skill to revise section 1.1, Latar Belakang, in the attached draft. Keep the numbers, citations, and method unchanged.

> Use the skripsi skill to assess whether the attached article can be a primary reference. Report journal indexing evidence separately from the article's relevance and quality.

> Use the skripsi skill to check consistency across Chapter III, the results, conclusions, and abstract. Report each finding with its evidence before proposing edits.

Thesis text is written in formal Indonesian. The agent uses the user's language for work notes and explanations.

## Contents

- [SKILL.md](SKILL.md): core instructions and module map.
- [`references/`](references/): academic rules, chapter guidance, writing style, citations, methods, and source checks.
- [`workflows/`](workflows/): research, writing, review, and revision procedures.
- [`templates/lembar-kerja.md`](templates/lembar-kerja.md): worksheets and structured report formats.
- [`checklists/audit-akhir.md`](checklists/audit-akhir.md): final checks.
- [`agents/openai.yaml`](agents/openai.yaml) and [`assets/icon.svg`](assets/icon.svg): agent listing metadata and icon.

Keep the directory structure so relative links between modules continue to work.

## Limits

The 2025 profile is a starting point, not proof of current submission requirements. Check the latest official rules before submitting or assessing compliance. Keep supervisor instructions and writer preferences separate from academic requirements.

Examples and placeholders are not research data. An audit covers only the material and evidence examined. Rule IDs identify review findings; they are not citations for the thesis.
