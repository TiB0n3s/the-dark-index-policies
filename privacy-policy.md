---
title: Privacy Policy
permalink: /privacy-policy/
---

# The Dark Index Privacy Policy

Effective date: July 27, 2026

The Dark Index is a private-first mobile application for cataloguing a physical
book collection. This policy describes the Core beta build.

## Information stored on your device

The app stores collection records, book and edition information, physical-copy
locations, notes, tags, lists, and preferences on your device. This information
supports offline collection access, browsing, searching, editing, duplicate
warnings, and manual export.

The Dark Index does not receive this information: there is no account, cloud
backup, or synchronization, and your collection records, shelf names, notes,
tags, and search activity never leave your device. The one exception is
described in "Book metadata lookup" below.

## Book metadata lookup

When you scan or add a book that is not already in your library, the app
sends **only the book's ISBN** to a catalogue lookup service operated by Dead
Star Labs, to retrieve publicly available edition details — title, author,
format, and similar fields — from Open Library and the Library of Congress.
This is a core part of how the app fills in a new book and has no on/off
setting; it happens only for books not already in your collection, and it
never runs for a book you already own.

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

## Cloud and subscriptions

Archivist and Collector capabilities are not operational in the Core beta. No
cloud account is created automatically, and the beta does not upload
collection data to a Dark Index service — the ISBN lookup described above is
the only outbound network request the app makes, and it never carries
collection data, only the ISBN itself. This policy will be revised before
account, billing, cloud, notification, or remote-diagnostics features are
enabled.

## Retention and deletion

Core beta data remains on the device until you edit or delete records, clear
the app's data, or remove the app. Manual CSV and JSON export is available
without a subscription.

Because the Core beta has no Dark Index account or remote collection store,
there is no remote account record to delete.

## Children

The app is not designed to collect personal information from children. The
Core beta does not operate an account or remote collection service.

## Changes

Material privacy changes will be reflected in the published policy before the
corresponding behavior is enabled.

## Contact

Questions about this policy or The Dark Index's privacy practices:
[support@deadstarlabs.com](mailto:support@deadstarlabs.com)

Support information is published at the
[support policy page](../support-policy/).
