# Deduplication Rules

Apply these rules before finalizing the test case table.

## Duplicate Detection

Treat cases as duplicates when they have the same:

- Feature/module.
- User role or permission context.
- Preconditions.
- Action under test.
- Input category.
- Expected result.

Different wording alone does not justify a separate test case.

## Merge Similar Cases

Merge cases when they test the same behavior and only differ by minor examples. Put multiple representative values in `Test Data`.

Example:

- Duplicate: one case for invalid email `abc`, another for invalid email `abc@`, another for invalid email `abc.com`.
- Better: one invalid email format case with `abc`, `abc@`, `abc.com` listed in `Test Data`.

## Keep Separate Cases

Keep cases separate when any of these change meaningfully:

- Role, permission, or record ownership.
- Status or workflow stage.
- Validation rule or boundary.
- Error message or expected system behavior.
- Business risk or severity.
- UI behavior vs backend/API validation behavior.
- Save/submit/delete outcome.

## Quality Gate

Each final test case must answer:

- What requirement, business rule, mockup element, or QA risk does this cover?
- Would a manual QA engineer know exactly how to execute it?
- Is the expected result observable and specific?
- Does another case already prove the same behavior?
- Can this case fail independently and provide useful information?
