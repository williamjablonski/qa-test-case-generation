# QA Test Case Generation Skill

A reusable Agent Skill for generating professional manual QA test cases from requirements, BRDs, user stories, acceptance criteria, spreadsheets, live mockup/prototype URLs, uploaded mockups, screenshots, wireframes, and existing test case templates.

The skill guides an AI agent to act like a senior QA engineer: analyze requirements carefully, inspect live or uploaded mockups, compare UI behavior against requirements, identify assumptions and clarifications, generate complete non-duplicated test cases, and produce output that is ready for Excel, Google Sheets, or a test management tool.

## What It Covers

- Requirement analysis and feature extraction
- Live mockup/prototype URL observation
- Uploaded mockup, screenshot, and wireframe comparison
- Positive, negative, boundary, validation, permission, workflow, UI, and data persistence cases
- Search, filter, sorting, pagination, reset, save, submit, cancel, edit, delete, approval, and rejection flows
- File uploads, exports, downloads, attachments, date rules, numeric fields, dropdowns, multi-selects, duplicate records, and backend validation risks
- Deduplication rules so repeated or overlapping cases are merged
- Clarifications, assumptions, missing requirements, and suggested improvements

## Installation

### Codex

```bash
mkdir -p ~/.codex/skills
git clone https://github.com/williamjablonski/qa-test-case-generation.git ~/.codex/skills/qa-test-case-generation
```

### Claude Code

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/williamjablonski/qa-test-case-generation.git ~/.claude/skills/qa-test-case-generation
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

### Live Mockup URL Example

```text
Use the qa-test-case-generation skill.

Requirement sheet: [provided by user]
Mockup URL: https://lease-request-hub.lovable.app/contracts
Template: [optional]
```

Expected behavior: the skill opens the URL, observes the Contracts page, identifies tables, filters, buttons, statuses, actions, modals, and workflows, compares them with the requirement sheet, then generates complete manual QA test cases with requirement and mockup traceability.

## Recommended Inputs

- Requirements sheet or document: `.xlsx`, `.csv`, `.docx`, `.pdf`, `.md`, ticket text, BRD, or user stories
- Optional live mockup/prototype URL, for example a Lovable, Figma prototype, staging, or demo link
- Optional uploaded mockups: screenshots, wireframes, UI designs, or prototype captures
- Optional existing test case template: Excel, CSV, Markdown, or test management export
- Optional existing test cases, user roles, permissions, business rules, API documentation, and acceptance criteria

## Live Mockup URL Behavior

When a live mockup/prototype URL is provided, the skill instructs the agent to:

- Open the URL and inspect the visible UI as a QA engineer.
- Navigate available pages, tabs, menus, buttons, modals, forms, tables, filters, action menus, and links.
- Record visible screens, UI elements, states, statuses, fields, controls, tables, filters, sorting, pagination, upload/download areas, and navigation elements.
- Compare the observed UI against the written requirements.
- Generate requirement-based, UI-based, and requirement-vs-UI gap test cases.

The agent should interact carefully with live mockups. It may open menus, dropdowns, modals, filters, and non-destructive controls to discover behavior, but it should not submit destructive actions or delete real data unless the environment is clearly a mock/demo environment and the user explicitly allows it.

## Limitations

- If the URL requires login and credentials are not provided, the skill marks the URL as inaccessible and asks for credentials or screenshots.
- If a page is blank, fails to load, has broken navigation, or does not allow real interactions, the skill documents the limitation and continues with available information.
- Accessibility observations are lightweight and based only on what is visible or reasonably testable from the mockup. Unverified items are marked as `Needs validation`.

## Output Sections

The skill asks the agent to return:

1. Requirement Summary
2. Live Mockup Observation Summary, when a live URL is provided
3. Requirement vs Mockup Gap Analysis, when mockups or URLs are provided
4. Assumptions
5. Clarifications Needed
6. Coverage Areas or Test Coverage Strategy
7. Test Cases Table
8. Missing/Unclear Requirements
9. Suggested Improvements or Missed Risks / Additional QA Suggestions

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
│   ├── deduplication-rules.md
│   └── live-mockup-url-review.md
└── examples/
    └── sample-output.md
```

## License

MIT
