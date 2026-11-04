# Tally
**Your spending, without the noise.**

**A calm Windows spending journal, subscription tracker and desktop companion.** Tally opens as a small widget, stays out of the way, and keeps your expenses, recurring bills and receipt photos together on your PC.

**Windows 10/11 x64 · Local-first · No account · No banking connection · Beta 1**

## Download Tally Beta 1

| Choose | Download | Where your records live |
|:--|:--|:--|
| **Portable ZIP** — extract and run, no installation | **[Download portable ZIP](https://github.com/memeseonew-eng/Tally/releases/download/v0.5.0-beta.1/Tally-Portable-v0.5.0-beta.1-win-x64.zip)** | `data/` beside `Tally.exe` |
| **Windows Setup** — shortcuts, simple updates, per-user install | **[Download Windows installer](https://github.com/memeseonew-eng/Tally/releases/download/v0.5.0-beta.1/Tally-Setup-v0.5.0-beta.1-win-x64.exe)** | `%LOCALAPPDATA%\Tally\data` |

**[Beta 1 release notes](https://github.com/memeseonew-eng/Tally/releases/tag/v0.5.0-beta.1)** · **[All versions](https://github.com/memeseonew-eng/Tally/releases)** · **[SHA256 checksums](https://github.com/memeseonew-eng/Tally/releases/download/v0.5.0-beta.1/SHA256SUMS.txt)**

*This is an unsigned early beta. Windows may warn about an unrecognized publisher. Download only from the official release, verify the SHA256 checksum, and don't disable your security protections.*

---

## A little clarity, every day

![Tally Overview — upcoming bills and recorded spending](screenshots/tally-overview.png)
*Everything in context: actual spending, the next payment, and 30-day/365-day scheduled forecasts. Screenshots use illustrative demo data.*

### Keep it on your desktop

Tally starts as a discreet **desktop widget**. See your spending at a glance, add an expense, then return to your day. Select **recent Week / Month / Year** without losing the separate current-month total. Open the full app with the small arrow icon, or hide the widget to the Windows tray.

<img src="screenshots/tally-widget.png" width="350" alt="Tally calm desktop widget with recent spending, category icons, and quick expense entry">

The widget can optionally show upcoming bills, top spending categories, or more recent entries — **none of these extras are forced on first launch.**

### Your spending, with a real timeline

![Tally Expenses — monthly spending charts and category breakdown](screenshots/tally-expenses.png)
*Week, Month and Year views, categories, totals and transactions. Currency totals are always separate.*

Record everyday purchases, search the ledger, choose from **27 category icons** (including Game), and see where the money went. Add up to **three local photos per expense** — useful for receipts and things worth remembering. Paid subscription records appear in actual spending only when you explicitly mark them paid.

### Make it yours. Or don't change a thing.

![Tally optional Style Studio — accent swatches, widget titles, badges and preview](screenshots/tally-personalization.png)
*An optional customization panel, shown with an example lilac style. The understated original is the default.*

- Choose a local background photo; fine-tune **blur and panel opacity**.
- Pick an accent, or enter your own hex color.
- Personalize the widget title and short note.
- Choose rounded, circle or square category badges.
- Save up to eight looks and **return to the base design in one click**.

No dozens of overwhelming themes. Just a quiet default and thoughtful optional finishing touches.

### Your file, your records, your backup

![Tally local data and recovery backup screen](screenshots/tally-data-backup.png)
*Local database snapshot and recovery controls.*

Tally needs **no account, cloud login, API subscription or bank access**. It stores records in a local SQLite file plus optional images and preference files. Before destructive removal, Tally creates a recovery snapshot. You can also save a database snapshot from Settings or create a **full data-folder ZIP** (including receipts and preferences) after quitting the app.

The Windows installer **does not delete your data when uninstalled**. Moving from portable to setup? Quit both editions and copy the whole data folder to the installed location. Do not overwrite two independently edited datasets.

---

## What makes Tally different?

| | |
|---|---|
| **Widget-first, not dashboard-first** | A tiny companion until you need the full ledger |
| **Actual vs. expected** | Recorded purchases never silently become future forecasts; scheduled bills aren't automatically considered paid |
| **Personal, optional style** | Liquid-glass-inspired neutral layout with background photos, blur, badges and saved looks |
| **Receipts that stay local** | Up to three managed photo attachments per expense |
| **Simple backup story** | A predictable data folder, guarded SQLite writes and recovery before removal |
| **Exact, separate currencies** | No invented exchange rates or misleading mixed-currency totals |
| **Offline by design** | No required server, banking connector, cloud account or background release check |

## Install and update

**Portable:** Extract the complete ZIP into a writable folder (e.g., Documents), then open `Tally.exe`. Keep the entire extracted folder, especially `data/`. For a full data ZIP, quit Tally and run `Backup-Tally.cmd`. To update, close Tally and replace only the app files, not your `data/` folder.

**Setup:** Run the installer. It installs for the current Windows user without administrator access and stores user records separately at `%LOCALAPPDATA%\Tally\data`. Use the **Back up Tally data** Start menu shortcut after quitting Tally. Updating or uninstalling the app does not remove your data folder.

Tally's own **Settings → Additional · Beta & updates** panel shows the installed version and links to this release and the version history. Updates are manual for this beta.

## Beta notes

Tally is an early Windows x64 beta. It does **not** automatically read bank transactions, detect settled payments, perform currency conversion, synchronize data between computers, or provide certified reminders. The desktop widget is an independent floating WPF window, not embedded into the Explorer desktop layer; multi-monitor behavior and Win+D persistence still need broader validation. The app and installer are currently **unsigned**. For problems, please use [GitHub Issues](https://github.com/memeseonew-eng/Tally/issues), but **never post your personal `data/` folder, receipts or bank information in an issue**.

## License and resources

Tally's original application binaries, icons, design assets and compiled shaders are distributed under **[proprietary end-user terms](LICENSE.txt)**. This public repository is a binary release and product information hub — **not an open-source code repository**. Third-party .NET and SQLite components retain their own separate licenses; see [notices](THIRD-PARTY-NOTICES.txt).

© 2026 Tally contributors. All rights reserved.
