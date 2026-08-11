---
title: Support Policy
permalink: /support-policy/
---

# The Dark Index Support Policy

Last reviewed: August 11, 2026

## Support boundary

Core supports local collection, shelf/location naming, ISBN capture, manual
entry, browsing, searching, duplicate warnings, and manual CSV/JSON export.
Archivist subscriptions and opt-in encrypted cloud backup are operational on
the supported store platforms.

Multi-device synchronization, version history, alerts, and the Collector plan
are unavailable in the shipping configuration. Variant identification and
local collection documentation exist behind exact Collector entitlements that
are not currently sold or granted. Their support procedures below become
customer-facing only after the remaining Collector gates are approved.

## User recovery steps

### Camera permission

1. Open the device settings for The Dark Index.
2. Allow Camera permission.
3. Return to the app and reopen ISBN scanning.
4. If scanning remains unavailable, use manual entry.

### On-device storage warning

1. Stop adding or editing records after a storage warning.
2. If export remains available, export both CSV and JSON.
3. Restart the app and device.
4. Confirm that an existing record can be opened and a harmless edit persists
   after another restart.
5. Escalate if the warning returns or records are missing.

### Import/export

- Keep a copy of exported files outside the app.
- CSV and JSON export remain Core capabilities.
- The current structured import accepts JSON, not CSV.
- Import location questions require the user to map a source path to an
  existing local location.

### Collection documentation

- A package is created only after the owner selects at least one eligible
  copy. Records explicitly marked not owned cannot be included.
- Generation requires the `collection.insurance_reports` entitlement, but no
  account, internet connection, insurer, appraiser, or valuation provider.
- One action creates PDF, CSV, and JSON together. Keep all three: PDF is the
  readable report, while JSON is the complete structured record and retains
  evidence-photo bytes.
- If generation fails, confirm that local storage is readable, at least one
  copy remains selected, and the destination share/save sheet is available.
  The failure message means nothing was uploaded; this feature has no upload
  path.
- Subscription cancellation stops new generation. It does not lock the local
  collection, owner evidence, or any PDF/CSV/JSON file already saved outside
  the app.
- Support cannot describe the package as an appraisal, proof of ownership,
  proof of coverage, a guaranteed value, or an insurance claim; interpret a
  policy; advise whether an insurer will accept a record; or file, negotiate,
  submit, or track a claim. Direct those questions to the user's insurer or a
  qualified appraiser.

### Suspected data loss

Do not clear app storage or reinstall until any available export and diagnostic
information have been preserved. Record the device model, OS version, app
version/build, last known successful action, and exact warning text.

## Response priorities

| Severity | Example | Target handling |
|---|---|---|
| Critical | Repeatable deletion/corruption affecting multiple records | Stop distribution, preserve evidence, begin incident process |
| High | App cannot open local storage or export | Triage before the next beta build |
| Normal | Camera, copy, visual, or isolated workflow issue with workaround | Record and prioritize in the beta backlog |

## Contact

Report issues or request help:
[support@deadstarlabs.com](mailto:support@deadstarlabs.com)

Include the device model, OS version, app version/build, and the exact text of
any warning when reporting a problem.
