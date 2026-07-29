---
title: Privacy Policy
permalink: /privacy-policy/
---

# The Dark Index Privacy Policy

Effective date: July 28, 2026

The Dark Index is a private-first mobile application for cataloguing a physical
book collection. This policy describes the current build: the Core experience,
which is entirely on your device apart from ISBN lookup, and the Archivist
capabilities that are operational — including encrypted cloud backup, which is
off unless a subscriber turns it on.

## Information stored on your device

The app stores collection records, book and edition information, physical-copy
locations, notes, tags, lists, and preferences on your device. This information
supports offline collection access, browsing, searching, editing, duplicate
warnings, and manual export.

By default The Dark Index does not receive this information: no account
exists, nothing is uploaded, and your collection records, shelf names, notes,
tags, and search activity never leave your device. There are two exceptions,
both described below. **Book metadata lookup** is part of adding a book and
sends only an ISBN. **Encrypted cloud backup** is off until you set it up,
and what it sends cannot be read by anyone but you.

## Book metadata lookup

When you scan or add a book that is not already in your library, the app
sends **only the book's ISBN** to a catalogue lookup service operated by Dead
Star Labs, to retrieve publicly available edition details — title, author,
format, cover image address, and similar fields — from Open Library and the
Library of Congress. This is a core part of how the app fills in a new book
and has no on/off setting; it happens only for books not already in your
collection, and it never runs for a book you already own — with one
exception, entirely under your control: if you explicitly run **"Find
missing covers"** in Settings, the app sends the ISBNs of books already in
your library that have no cover image, one at a time, to the same service,
to retrieve their cover addresses. That action states how many ISBNs it will
send before anything is sent, runs only when you start it, and sends nothing
else about your library. It never runs on its own.

No account, device identifier, advertising identifier, or IP address is
retained by this lookup. The service does not know who is asking, and there
is no record tying any lookup to you individually — it keeps only the edition
data itself, so future scans of the same book by anyone are faster. The
server records when it last learned about an edition, rounded to the day, so
it knows when to refresh a stale entry; it does not keep a log of individual
requests or scan times. The service is hosted in the European Union, and the
reverse proxy in front of it does not log the IP address of any request,
matched or not, for the same reason.

## Camera access

Camera access is used only when you choose ISBN scanning. Barcode frames are
processed to find an ISBN. The app does not intentionally retain photographs,
video, or camera frames. You can deny camera access and enter a book manually.

## Files you choose

When you export data, you choose where the CSV or JSON file is sent or saved.
When structured import becomes available to an entitled user, the user chooses
the JSON file. The destination application or storage provider you select may
apply its own privacy practices.

## Analytics and advertising

The Core beta does not collect usage analytics, use advertising identifiers,
serve advertising, or remotely log collection titles or searches.

## Subscriptions and purchases

Archivist subscriptions are purchased through Apple's App Store or Google
Play. The purchase happens entirely in your store account: Dead Star Labs
receives no payment details, creates no account of you, and operates no
purchase server — whether a subscription is active is determined by your
store, on your device, and the app keeps only your current entitlement
locally so it works offline. Apple's and Google's own privacy terms govern
the transaction, as with any store purchase. Managing or cancelling happens
in your store's subscription settings.

## Cover images

When your plan shows photo book covers, the app fetches the cover image
from Open Library's public covers service (`covers.openlibrary.org`), the
same way any app loads an image from the web: the request carries the
image's address and your device's network address, and no account or
identifier. Without a plan that shows photo covers, no such request is
made.

## Encrypted cloud backup

Encrypted backup is an Archivist capability, and it is **off until you set
it up**. Until then nothing is uploaded, no account exists, and the app
makes no request to the backup service at all.

**Your collection is encrypted on your device before it leaves it.** What
travels, and what the service stores, is ciphertext. Dead Star Labs holds no
key that opens it. An operator with full access to the server's database,
its files, and its source code can demonstrate only encrypted bytes.

**Setting up backup creates an account, and that account has no idea who you
are.** It is identified by a value derived from your recovery key. We do not
ask for, and the service never receives, an email address, a name, a phone
number, or a device identifier.

| The backup service stores | It never stores |
|---|---|
| Your encrypted snapshot | Your collection in readable form |
| An account identifier | Your name, email, or phone number |
| A hash of your authentication key | Your recovery key, or anything that could open your backup |
| When your subscription runs through | Your IP address |
| A salted hash of your store transaction | Your raw store receipt |
| The size and date of your snapshot | The titles, notes, or shelves inside it |

The service is hosted in the European Union, on separate infrastructure from
the ISBN lookup service described above, with no shared database or
credentials. The two cannot be combined to link a book you looked up with a
backup you made. As with the lookup service, the reverse proxy in front of
it logs no IP addresses, for any request, matched or not.

**Your recovery key is the only way in, and we cannot recover it for you.**
There is no password reset, no email recovery, and no support process that
can restore access — because any such process would mean we could read your
backup, and we cannot. If you lose the recovery key, the backup becomes
permanently unreadable. This is shown once during setup and requires you to
confirm you have written it down.

**A store transaction is linked to your account by a salted hash**, so that
storage is provided to subscribers rather than to anyone who asks. The raw
receipt is not stored, and the hash cannot be reversed into your store
account.

**If your subscription lapses, your backup is not deleted immediately.** It
remains restorable for 90 days, during which new backups will not upload.
After 90 days the stored snapshot is deleted.

**Deleting your backup deletes everything associated with it** — the
encrypted snapshot, the account record, and the transaction hash. You can do
this at any time from Settings, and it does not require an active
subscription: the person most likely to want their data removed is the one
who has stopped paying for it. Your collection stays on your device. See
[how to delete your account and data](../delete-account/).

**Nothing uploads on its own.** Backup runs when you choose to run it. There
is no schedule, no background upload, and no automatic sync — so the way to
stop backing up is simply to stop, and what is already stored stays until you
delete it.

Restoring on a second device is not synchronization: two devices backing up
one account overwrite each other's snapshots, and the app says so before you
restore.

## Cloud features not yet operational

Multi-device synchronization, version history, and Collector capabilities are
not operational. This policy will be revised before those, or notification or
remote-diagnostics features, are enabled.

## Retention and deletion

On-device data remains on the device until you edit or delete records, clear
the app's data, or remove the app. Manual CSV and JSON export is available
without a subscription.

**If you have not set up encrypted backup, there is no remote record of you
to delete** — no account exists and nothing has been uploaded.

If you have set up encrypted backup, deleting it removes the encrypted
snapshot, the account record, and the store-transaction hash. A lapsed
subscription retains the snapshot for 90 days, then deletes it. Full steps
are on the [account and data deletion page](../delete-account/).

## Children

The app is not designed to collect personal information from children. The
only account it can create is the encrypted-backup account described above,
which holds no name, email, or other personal information, and which exists
only if an adult subscriber sets it up.

## Changes

Material privacy changes will be reflected in the published policy before the
corresponding behavior is enabled.

## Contact

Questions about this policy or The Dark Index's privacy practices:
[support@deadstarlabs.com](mailto:support@deadstarlabs.com)

Support information is published at the
[support policy page](../support-policy/).
