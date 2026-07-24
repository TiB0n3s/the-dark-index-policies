---
title: Support Policy
permalink: /support-policy/
---

# The Dark Index Core Beta Support Policy

## Support boundary

The Core beta supports local collection, shelf/location naming, ISBN capture,
manual entry, browsing, searching, duplicate warnings, and manual CSV/JSON
export.

Billing, subscriptions, accounts, cloud backup, multi-device synchronization,
automatic metadata lookup, alerts, and Collector services are unavailable.

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
