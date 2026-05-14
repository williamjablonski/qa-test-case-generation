# Live Mockup URL Review

Use this checklist when the user provides a live mockup or prototype URL in addition to, or instead of, uploaded mockup files.

## Input Handling

- Treat the URL as an optional mockup source, not as a replacement for the required requirements, BRD, user story, feature description, or acceptance criteria.
- If requirements are missing, ask for them or clearly state that test cases will be UI-observation based and limited.
- If credentials are required and not provided, mark the URL as inaccessible and ask for credentials or screenshots.

## Observation Workflow

1. Open the provided URL.
2. Record the URL, page title, first visible page, and any load/authentication issues.
3. Navigate through visible pages, tabs, menus, sidebar items, header links, breadcrumbs, buttons, action menus, and table links.
4. Open non-destructive modals, drawers, dropdowns, date pickers, filter panels, action menus, and expandable sections to observe available controls.
5. Record each visible screen/page and the UI elements on it.
6. Note unclear, broken, disabled, read-only, inaccessible, or non-interactive areas.
7. Compare observations against the provided requirements before generating test cases.

## UI Elements to Record

- Navigation elements, tabs, breadcrumbs, menus, links, icons, and action menus.
- Forms, fields, labels, placeholders, required indicators, help text, validation messages, and read-only fields.
- Buttons, disabled buttons, submit/save/cancel controls, destructive actions, confirmation dialogs, and success/error messages.
- Dropdowns, checkboxes, radio buttons, multi-selects, date pickers, upload fields, attachment controls, and download/export/import controls.
- Tables, columns, rows, status labels, badges, sorting controls, pagination, page-size controls, search inputs, filters, reset/clear controls, and empty states.

## UI States to Look For

- Empty, loading, disabled, read-only, error, success, draft, submitted, pending, approval, rejected, cancelled, and completed states.
- No-result states after search/filter when safe to test.
- Validation states for required fields or invalid values when validation can be triggered without creating destructive data.
- Unsaved-change, confirmation, and recovery states when visible.

## User Flows to Infer

- Create, view, edit, delete, search, filter, sort, submit, cancel, approve, reject, upload, download, open attachment, view attachment, export, import, pagination, and navigation flows.
- Permission, ownership, read-only, and status-transition flows when visible or implied.
- Regression risks from data persistence, refresh/reopen behavior, duplicate actions, and repeated clicks.

## Safe Interaction Rules

- Click buttons only when needed to discover UI behavior.
- Open menus, dropdowns, filter panels, modals, and drawers to observe available options.
- Do not submit destructive actions, delete data, approve/reject real records, or send real notifications unless the environment is clearly a mock/demo environment and the user explicitly allows it.
- If destructive behavior would be useful to test, document it as a suggested test case instead of performing it.
- If the prototype does not allow real interactions, note the limitation and generate test cases from visible UI plus requirements.
- If navigation is broken or a control does nothing, document it as a possible bug, risk, or clarification item.
- If behavior is unclear, mark it as `Needs clarification`.

## Requirement vs Mockup Matching

When requirements and the URL are both available, produce these findings:

- Requirements found in the mockup: requirements clearly represented by visible UI or discoverable interactions.
- Requirements missing from the mockup: requirements that are not visible, not reachable, or not testable in the live UI.
- Extra UI elements in the mockup: controls, pages, fields, statuses, or workflows not mentioned in requirements.
- Conflicts or inconsistencies: label mismatches, missing fields, different statuses, wrong field types, unexpected buttons, missing buttons, unclear validation, inconsistent workflow order, or ambiguous permissions.
- Questions/clarifications: items requiring confirmation from the product owner, BA, designer, or developer.

## Accessibility and Usability Checks

Make lightweight observations only when visible or reasonably testable:

- Field labels, required field indicators, placeholder clarity, and form grouping.
- Button text clarity and icon meaning.
- Error message visibility and placement.
- Color/status clarity and whether meaning appears to rely only on color.
- Table readability, column naming, alignment, and scanability.
- Navigation clarity, disabled button clarity, and basic keyboard/navigation concerns if observable.

Do not make accessibility claims that cannot be verified from the mockup. Mark uncertain findings as `Needs validation`.

## Error Handling

Continue with available information and clearly mention limitations when:

- The URL is inaccessible, requires login, is blank, or fails to load.
- The page loads but no useful UI appears.
- Buttons, pages, menus, or links do not work.
- Some pages are unavailable.
- The prototype does not allow real interactions.
- Requirements are missing, conflict with the mockup, or do not mention visible features.
- The mockup contains features not mentioned in requirements.

## Example

Input:

- Requirement sheet: provided by user
- Mockup URL: `https://lease-request-hub.lovable.app/contracts`
- Template: optional

Expected behavior:

Open the URL, observe the Contracts page, identify tables, filters, buttons, statuses, actions, modals, and workflows, compare them with the requirement sheet, then generate complete manual QA test cases with requirement and mockup traceability.
