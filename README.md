# Skripsi

An [agent skill](SKILL.md) for researching, writing, revising, and reviewing an undergraduate Information Systems thesis. It covers literature, journal selection, IEEE citations, Chapters I–V, research methods, and thesis defenses. Its default academic profile is the Solusi track at UPN Veteran Jawa Timur, based on 2025 materials.

## Install

```sh
npx skills add wahyuabrory/skripsi-pacil --skill skripsi
```

You can also point an agent to [SKILL.md](SKILL.md) and use the skill without installing it. There is no bootstrap step, required service, or software package for the skill itself.

## First use

Give the agent the draft, data, or source to work on. Name the target section and any limits on the change. For example:

> Use the skripsi skill to revise section 1.1, Latar Belakang, in the attached draft. Keep the numbers, citations, and method unchanged.

The agent starts at `SKILL.md` and reads the relevant modules, not the whole repository. Thesis text is written in formal Indonesian. Work notes and explanations follow the user's language.

## What it can do

| Request | Expected output |
| --- | --- |
| Plan a proposal or research workflow | A scoped plan tied to the research problem and available evidence |
| Search literature or assess a journal | Candidate sources or a journal assessment that separates indexing evidence from article quality |
| Write or revise a section | Indonesian text ready to use, with missing evidence marked rather than invented |
| Check citations or formatting | Specific issues and corrections against the applicable guidance |
| Audit a draft | Findings with location, evidence, rule ID, severity, and action |
| Prepare for a proposal seminar or final defense | Preparation based on the available draft and verified rules for that stage |

Example audit request:

> Use the skripsi skill to check consistency across Chapter III, the results, conclusions, and abstract. Report each finding with its evidence before proposing edits.

## Evidence and scope

The skill distinguishes academic requirements, writer preferences, presentation patterns, and additional verification practices. An audit covers only the material and evidence supplied or checked. It does not issue a blanket compliance verdict for an unseen thesis.

It preserves names, numbers, methods, and citation identities from the source material. Missing sources, data, confirmation, or tests are marked in a working draft instead of filled with invented results. Rule IDs identify review findings; they are not citations for the thesis.

The 2025 profile is a starting point, not proof of current submission requirements. Check the latest official rules before submitting or assessing compliance. If supervisor instructions conflict with verified academic rules, resolve the conflict rather than silently choosing one.

## Repository layout

| Path | Purpose |
| --- | --- |
| [SKILL.md](SKILL.md) | Entry point, core behavior, and module map |
| [references/](references/) | Academic rules, chapter guidance, style, citations, methods, and source checks |
| [workflows/](workflows/) | Research and writing flow; review and revision flow |
| [templates/lembar-kerja.md](templates/lembar-kerja.md) | Worksheets and structured report formats |
| [checklists/audit-akhir.md](checklists/audit-akhir.md) | Final checks |
| [agents/openai.yaml](agents/openai.yaml) and [assets/icon.svg](assets/icon.svg) | Agent listing metadata and icon |

Keep the directory structure so relative links between modules continue to work.

## License

[MIT](LICENSE).
