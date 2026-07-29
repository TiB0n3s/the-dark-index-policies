---
title: Delete Your Account and Data
permalink: /delete-account/
---

# Deleting your account and data

**App:** The Dark Index
**Developer:** Dead Star Labs

## Most people have no account to delete

The Dark Index creates an account only if you set up **encrypted cloud
backup**, an Archivist subscription feature that is off unless you turn it
on. If you have never set it up, no account of you exists, nothing of yours
has been uploaded, and there is nothing here to delete. Your collection lives
on your device and is removed by deleting the app or clearing its data.

## How to delete your backup account

1. Open **The Dark Index** on the device where backup is set up.
2. Go to **Settings → Encrypted backup**.
3. Tap **Delete backup and account**.
4. Confirm. Deletion happens immediately.

You do **not** need an active subscription to do this. If your Archivist
subscription has lapsed, deletion still works — the person most likely to
want their data removed is the one who has stopped paying for it.

## What is deleted

Deleting removes all of it, immediately and permanently:

- **The encrypted snapshot of your collection** — the stored backup itself.
- **The account record** — the account identifier and the hash of your
  authentication key.
- **The salted hash of your store transaction**, which existed only to
  confirm a subscription was paying for the storage.

Nothing of yours remains on the service afterwards, and no additional
retention period applies to deleted accounts.

## What is kept, and where

**Your collection stays on your device.** Deleting the backup removes what
the service holds, not what you own. To remove the collection itself, delete
the app or clear its data on the device.

Your **recovery key** stops opening anything, on every device. The account is
the recovery key, so deleting reaches any other device that used the same
key — not only the one you delete from.

## If your subscription lapses without you deleting

A lapsed subscription does not delete your backup straight away. The stored
snapshot remains restorable for **90 days**, during which no new backups
upload. After 90 days it is deleted automatically, along with the account
record and transaction hash.

## Why we cannot delete it for you

The backup service holds no email address, name, phone number, or device
identifier — by design, so that a stored backup cannot be traced to a person.
The consequence is that **we cannot identify which account is yours**, and so
we cannot delete one on your behalf. There is no support process that can,
and any process that could would mean we were holding information this
product deliberately does not hold.

If you have lost the device and your recovery key, the stored data is already
unreadable to everyone including us. To have it removed, cancel the Archivist
subscription in your App Store or Google Play account; the backup is deleted
automatically 90 days later.

## Questions

[support@deadstarlabs.com](mailto:support@deadstarlabs.com)

We can walk you through the steps above. We cannot perform the deletion for
you, for the reason given above.

See also the [privacy policy](../privacy-policy/).
