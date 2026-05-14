# Boundary and Edge Case Checklist

Use this checklist to generate focused boundary cases. Include boundaries that are logically relevant even when not explicitly stated, but document assumptions.

## Text Fields

- Empty value for required fields.
- Blank spaces only.
- Leading/trailing spaces.
- Minimum length minus one, minimum length, maximum length, maximum length plus one.
- Special characters such as `!@#$%^&*()_+-=[]{};':",.<>/?`.
- Unicode/non-English characters when the product supports international users.
- Very long pasted text.
- Duplicate names, case sensitivity, and whitespace-normalized duplicates.

## Numeric Fields

- Empty, zero, negative, decimal, very large number, non-numeric characters, scientific notation, and comma-formatted values.
- Minimum minus one, minimum, maximum, maximum plus one.
- Precision and rounding rules for currency, percentages, quantities, and measurements.

## Date and Time Fields

- Empty required date.
- Invalid date format.
- Start date after end date.
- Same start and end date.
- Past date, current date, future date, leap day, month/year boundary, and timezone-sensitive values.
- Expired dates and future-only/past-only restrictions.

## Dropdowns and Multi-Selects

- No selection, valid selection, all selections, max allowed selections plus one, duplicate selection, disabled option, and dependent option changes.
- Behavior when parent field changes after child field already has a value.

## File Uploads and Attachments

- No file, supported type, unsupported type, minimum/empty file, maximum size, size above maximum, multiple files, duplicate file names, special characters in file name, corrupted file.
- Preview, remove, replace, download, view attachment, and persistence after save/reopen.

## Search, Filter, Sort, Pagination

- Exact match, partial match, case differences, special characters, no results, cleared search.
- Single filter, multiple filters, invalid filter combination, reset filters.
- Ascending/descending sorting, sorting with empty values, sorting after filtering.
- First page, next page, previous page, last page, page size change, no records.

## Workflow and Permissions

- Unauthorized role, read-only role, owner vs non-owner, approver vs requester, inactive user.
- Valid transition, invalid transition, skipped transition, rejected record resubmission, cancelled record edit attempt.
- Direct URL/API access to restricted records.

## Rare User Behavior

- Double-click submit.
- Navigate away with unsaved changes.
- Browser refresh during form entry.
- Back button after submit.
- Concurrent edit by another user.
- Session timeout during save or approval.
