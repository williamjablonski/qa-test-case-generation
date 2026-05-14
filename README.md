# QA Test Case Generation Skill

A reusable Agent Skill for generating professional manual QA test cases from requirements, BRDs, user stories, acceptance criteria, spreadsheets, mockups, screenshots, wireframes, and existing test case templates.

The skill guides an AI agent to act like a senior QA engineer: analyze requirements carefully, compare mockups against requirements, identify assumptions and clarifications, generate complete non-duplicated test cases, and produce output that is ready for Excel, Google Sheets, or a test management tool.

## What It Covers

- Requirement analysis and feature extraction
- Mockup and screenshot comparison
- Positive, negative, boundary, validation, permission, workflow, UI, and data persistence cases
- Search, filter, sorting, pagination, reset, save, submit, cancel, edit, delete, approval, and rejection flows
- File uploads, exports, downloads, attachments, date rules, numeric fields, dropdowns, multi-selects, duplicate records, and backend validation risks
- Deduplication rules so repeated or overlapping cases are merged
- Clarifications, assumptions, missing requirements, and suggested improvements

## Installation

### Codex

```bash
mkdir -p ~/.codex/skills
git clone https://github.com/saleem-daqa/qa-test-case-generation.git ~/.codex/skills/qa-test-case-generation
```

### Claude Code

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/saleem-daqa/qa-test-case-generation.git ~/.claude/skills/qa-test-case-generation
```

### Update Later

```bash
git -C ~/.codex/skills/qa-test-case-generation pull
git -C ~/.claude/skills/qa-test-case-generation pull
```

## Example Prompt

```text
Use the qa-test-case-generation skill to generate complete manual QA test cases from requirements.xlsx and the attached mockups. Follow template.xlsx exactly. Include assumptions, clarifications needed, missing requirements, suggested improvements, and non-duplicated test cases ready for Excel.
```

## Recommended Inputs

- Requirements sheet or document: `.xlsx`, `.csv`, `.docx`, `.pdf`, `.md`, ticket text, BRD, or user stories
- Optional mockups: screenshots, wireframes, UI designs, or prototype captures
- Optional existing test case template: Excel, CSV, Markdown, or test management export

## Output Sections

The skill asks the agent to return:

1. Requirement Summary
2. Assumptions
3. Clarifications Needed
4. Coverage Areas
5. Test Cases Table
6. Missing/Unclear Requirements
7. Suggested Improvements

## Repository Structure

```text
qa-test-case-generation/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── assets/
│   └── default-test-case-template.md
├── references/
│   ├── qa-coverage-checklist.md
│   ├── boundary-edge-case-checklist.md
│   └── deduplication-rules.md
└── examples/
    └── sample-output.md
```

## License

MIT
