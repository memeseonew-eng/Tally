# Security and privacy

Tally is a local-first Windows desktop app. It has no built-in banking connector, user account, cloud sync or required background update check. The GitHub release links in Settings are opened **only if you click them**.

Your private data is stored in SQLite plus local photos and preferences. Please **never upload `tally.sqlite`, the `data/` folder, receipts or financial screenshots containing real information to a public GitHub issue**.

When reporting a bug:
- Describe steps, Tally version, Windows version and whether you're using portable or Setup.
- Attach sanitized screenshots only.
- Remove real names, merchants, dates, file paths and currency balances if needed.
- Use a fresh isolated demo dataset to reproduce whenever possible.

To make a complete backup, quit Tally and use the included full-data backup script. Treat resulting ZIP files as sensitive financial records. The Setup uninstall process deliberately leaves your per-user data folder intact.

The beta is not code-signed. Verify SHA256 hashes from the official release and do not disable Windows security to install untrusted downloads.

This release repository contains public binaries and product documentation only. Security issues may be reported via a GitHub issue without private data; for sensitive issues, request a private contact channel rather than publishing an exploit or financial information.
