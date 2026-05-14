# QA Coverage Checklist

Use this checklist to find coverage gaps after reading the requirements. Include only relevant cases; do not add irrelevant generic tests.

## Core Functional Coverage

- Happy path create/save/submit flows.
- View, edit, delete, cancel, reset, clear, and retry flows.
- Required and optional field behavior.
- Field dependencies and conditional visibility.
- Data calculations, default values, generated values, and uniqueness rules.
- Duplicate record handling.
- Success, warning, validation, and error messages.
- Confirmation popups and destructive action safeguards.
- Data persistence after save, refresh, logout/login, close/reopen, and navigation away/back.

## UI and Interaction Coverage

- Labels, placeholders, help text, icons, buttons, links, tabs, breadcrumbs, menus, and table headers.
- Required field indicators and disabled/enabled states.
- Layout, alignment, readability, responsiveness, and usability issues visible from mockups.
- Search, filter, sort, pagination, column visibility, empty states, and no-result states.
- Loading states and repeated clicks on submit/save buttons when relevant.

## Workflow and Business Rule Coverage

- Status transitions and invalid status transitions.
- Approval, rejection, return, escalation, assignment, reassignment, and cancellation workflows.
- Role-based and permission-based access.
- View-only behavior for unauthorized users or locked records.
- Dependencies between records, modules, fields, statuses, or previous test cases.
- Audit/history/logging expectations when stated or business-critical.

## Data and Integration Coverage

- Backend/API validation behavior when UI validation can be bypassed.
- Data formatting in lists, details pages, exports, downloads, and printed views.
- Import/export behavior, attachment handling, file preview, and download/view permissions.
- Cross-browser, device, or environment expectations if stated.
- Notifications, emails, SMS, webhooks, or downstream updates if relevant.

## Negative and Risk Coverage

- Invalid, missing, duplicate, expired, unauthorized, too-large, too-small, malformed, unsupported, and conflicting inputs.
- Permission attempts through direct URL/API access when relevant.
- Race conditions from double submission, stale data, or concurrent edits when business-critical.
- Recovery from validation errors without losing entered data.
