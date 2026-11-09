## 0.5.11-preview.36 — 2026-11-09

Changes since public Preview33:

- A restrained Liquid Glass-inspired widget, inset corners, soft perimeter and matching two-line resize grip.
- More legible small action buttons with safer padding and reduced curvature.
- Optional **Start with Windows** switch and startup-registration ownership protections.
- Full-opacity first Notes render and retained large-list virtualization.
- Notes library width 226 → 210 DIPs; long titles use bounded ellipsis.
- 160 ms fading/upward exit and continuous reversal for the Navigation recall control; pane hide/Join behavior preserved.
- Exact verified Preview36 application runtime packaged for Portable and per-user Setup.
- Stable Setup AppId, installation directory and separate personal profile support **manual in-place upgrades**, not automatic downloads.

[Preview36 release notes](RELEASE_NOTES_PREVIEW36.md) include test scope and boundaries. New public Setup execution/uninstall is **NOT_RUN**, though an earlier local Setup upgrade completed successfully.

---
## 0.5.11-preview.33 — 2026-11-07

Changes since public Preview27:

- Hide and recall the separated Navigation card without joining it; retain pane placement and compact-layout access.
- Keep large Notes libraries responsive with recycling virtualization.
- Export TXT/Markdown or delete a note from its library row or document tab; ordinary tab X still closes only the tab.
- Reorder Notes at same-folder row edges while preserving the center folder-creation action.
- Save display order for Transactions and active Subscriptions without changing financial dates, totals or payment history.
- Add lifted drag previews, moving neighbors and Escape cancellation.
- Remove the extra outer frame from lifted rows while keeping their original contour, content and intentional lift shadow.
- Keep attachment thumbnails, Collection photo icons and entry covers inside their intended rounded surfaces.
- Add horizontal widget transitions and brief menu, chart, progress, insights and guarded Quit motion.
- Keep one sliding Money/Daily selection highlight during hover and press, removing overlapping capsules during mode changes.
- Dismiss command-result notices automatically, including unsuccessful results, without weakening save or confirmation guards.
- Improve compact finance headers, insight text wrapping, input states and Korean Notes text.
- Include the self-contained x64 runtime 10.0.14.

See [release notes](RELEASE_NOTES_PREVIEW33.md) for scope and verification. Setup qualification is compilation/static checks only; fresh install/uninstall execution is **NOT_RUN**.

---

## Previous public release — 0.5.11-preview.27 (2026-11-06)

- Adds matching minimize/restore motion to joined and separate panes without changing native geometry or remembered placement.
- Completes and validates full-width fast caption capture and persistent joined/separated window positions, sizes, order and hidden Workspace state.
- Cancels stale minimize completions on restore/close/join and respects the Windows motion policy.
- Updates in-app official release URLs and public Portable/Setup/download metadata.
- No stock-chart provider, browser dependency, account integration or new option is bundled. Chart feasibility is tracked separately.

See [Preview27 release notes](RELEASE_NOTES_PREVIEW27.md).

---
# Current public release — 0.5.11-preview.25 (2026-11-06)

- Publishes the qualified Preview25 binary, adding Daily tasks, full Notes/folders/tabs/attachments and Collections since Beta2.
- Adds detachable navigation/workspace cards, deliberate 440ms release-to-join edge gestures, role-based X behavior and natural workspace reopening.
- Uses a 1040x700 logical default, consistent page/material motion, shared rounded editor surfaces and corrected dark focused fields.
- Updates public downloads, screenshots, manual, release notes and checksums. No private application source or personal data is published.
- Preview26 layout-memory/fast-drag work is intentionally NOT included until native acceptance completes.
- Packages are unsigned and self-contained (.NET/Windows Desktop 10.0.14). Installer compile and portable extraction are checked; fresh install/uninstall is not certified in this release run.

See [detailed release notes](RELEASE_NOTES_PREVIEW25.md).

---
# Tally release history

## 0.5.4 Beta 2 (2026-11-05)
Second public Windows x64 beta: the widget becomes a more useful independent companion while the default layout stays quiet.

- **Widget quick note:** Optional 1,500-character private scratchpad, autosave/manual save, guarded atomic updates and explicit recovery.
- **Direct widget management:** Edit/add everyday expenses and subscriptions, and confirm scheduled payments without opening the full workspace.
- **Single adaptive primary action:** The widget's large button changes between + Expense and + Subscription; duplicate small add actions were removed.
- **One-click widget close:** A dedicated X hides only the widget and preserves the tray and safe note closure.
- **Connected motion:** Widget-to-workspace opening and a complementary reverse close, subtle navigation and button feedback, and short native currency/category/billing/calendar *opening* animations.
- **Keyboard-safe dropdowns:** Escape/Tab and selection remain immediate; no delayed dropdown closing fade.
- **Distribution and privacy:** New self-contained Portable and Setup, public hashes and synthetic screenshots, no private code/data uploaded, manual update links.
- **Preserved foundations:** Currency-separated recorded spending, subscriptions, linked paid history, receipts, optional Style Studio, local SQLite and full-data backups.

## 0.5.0 Beta 1 (2026-11-05)
First public Windows x64 beta.

- **Distribution:** Portable ZIP, self-contained Windows Setup, direct release links, version information, public checksum and beta changelog.
- **Desktop companion:** Widget-first, one-click full app, independent Week/Month/Year recent activity, optional bill/category panels and safe tray hiding.
- **Everyday ledger:** Week/Month/Year totals, categories (including Game), search/filter, receipts (up to three local photos), notes and exact currency-separated sums.
- **Subscriptions:** Recurring schedules, rolling 30/365-day forecasts, manually recorded paid actions, archive and restore, retained payment history.
- **Make it yours:** Local background image, adjustable blur and opacity, neutral default, optional Style Studio accent/text/badge shapes and up to eight saved looks.
- **Local control:** SQLite with separate sidecars, recovery snapshot before protected removal, manual database backup and complete folder backup helper.
- **Updates:** Version and manual release links in Settings. No background internet checks.

### Earlier local development (not previously published)

0.5.0 WX01: selectable widget recent periods, optional category/upcoming modules, collapsed spending insights.
0.4.0 WS01: weekly recorded expenses, Game category, optional Style Studio.
0.3.2 WH01: tray-only Hide widget and compact full-app icon.
0.3.1 WF01: widget-first startup and one-click workspace.
0.3.0 WG01: first widget and local receipt journal, neutral defaults, category scroll improvement.
0.2.1 LG02: refined glass layout and icon categories.
0.2.0 SG01: local actual-expense ledger and user-selected wallpaper/blur.
0.1.x: recurring subscription engine, local backups and WPF foundation.

**Notes:** Beta releases may be marked as prereleases, which are not necessarily included in GitHub's `releases/latest` endpoint. Use the [All releases](https://github.com/memeseonew-eng/Tally/releases) page or pinned tag links. Public source code is not provided.
