# Default Manual Test Case Template

Use this table when the user does not provide a test case template. Preserve these columns unless the user asks for a different format.

| Test Case ID | Module / Feature | Test Scenario | Preconditions | Test Steps | Test Data | Expected Result | Priority | Severity | Test Type | Status | Notes |
|---|---|---|---|---|---|---|---|---|---|---|---|
| TC-MODULE-001 | Module name | Verify that... | User/system state required before execution | 1. Step one<br>2. Step two<br>3. Step three | Specific values, accounts, dates, files, or N/A | Verify that the exact observable result occurs, including messages, saved data, status, UI state, or backend behavior. | High | Major | Functional | Not Run | Requirement ID, mockup reference, assumption, or dependency |

## Field Guidance

- `Test Case ID`: Use a unique stable ID, usually `TC-<MODULE>-001`.
- `Module / Feature`: Name the screen, flow, API-backed feature, or business function.
- `Test Scenario`: Start with `Verify that...` and state one clear purpose.
- `Preconditions`: Include required role, existing data, status, configuration, or navigation state.
- `Test Steps`: Number each manual step. Keep steps executable and specific.
- `Test Data`: Use realistic data. Write `N/A` only when no data is needed.
- `Expected Result`: State the exact observable outcome. Avoid `works correctly`.
- `Priority`: Use `High`, `Medium`, or `Low`.
- `Severity`: Use `Critical`, `Major`, `Minor`, or `Trivial`.
- `Test Type`: Use categories such as `Functional`, `Negative`, `Boundary`, `Validation`, `UI`, `Permission`, `Workflow`, `Integration`, `Regression`, `Usability`, or `Data Persistence`.
- `Status`: Default to `Not Run`.
- `Notes`: Add requirement IDs, mockup references, assumptions, dependencies, or clarifications.
