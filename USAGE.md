# Using Tally

**0.5.11-preview.36 · 2026-11-09 · Windows x64 · Bundled runtime 10.0.14**

[Overview](README.md) · [Release notes](RELEASE_NOTES_PREVIEW36.md)

## Start with the right profile

The portable edition uses the writable **data/** folder beside **Tally.exe**. Extract the entire portable folder before launching; do not run inside the ZIP or copy only the executable. **Open-Full-Tally.cmd** opens the full workspace directly.

Setup shortcuts use **%LOCALAPPDATA%\Tally\data**. Setup and portable folders do not automatically share or import records. Settings & help identifies the active data location. Launching a different profile selects a different dataset; it does not move the original records.

Normal startup opens the desktop widget. Use its workspace launcher or the tray menu to open full Tally.

## Updated widget, Notes library and Windows startup

The widget retains Money/Daily and the existing content layout, now with a softer inset glass surface, a matching two-line resize grip and readable foreground text. Resize from its bottom-right corner when position locking is off.

The Notes library is intentionally slightly narrower at 210 DIPs. Long note titles end in ellipses, without changing their stored text; document tabs, virtualized rows and drag behavior remain intact. Initial document text no longer starts faded.

Use **Settings → Start with Windows** to enable or disable sign-in startup for the installed profile. The Setup does not switch it on automatically. This is not automatic version updating: obtain and run new installers from the official GitHub release page.
## Windows, cards and quitting

Use the split control to separate Navigation and Workspace. Drag their blank upper caption areas to move them. Buttons and the brand artwork are not interchangeable with those drag areas. Separated cards have a bottom-right resize handle.

| Action | Result |
| --- | --- |
| Navigation X, while separated | Hides Navigation without joining the cards. |
| Recall action in Workspace | Shows the hidden Navigation card again at its saved position. |
| Workspace X | Hides Workspace; select a navigation item or use the widget/tray launcher to return. |
| Join control | Combines Navigation and Workspace. |
| Widget X | Hides the widget while the tray remains available. |
| Quit Tally | Exits the application after pending-save and busy checks allow it. |

For edge joining, bring the facing left/right edges together, pause until the frosted cue is ready, then release. A quick pass, early release, retreat or Escape does not confirm a join.

Positions, sizes and hidden-pane state are remembered across restart. Tally recovers inaccessible placements when a monitor is no longer available. Closing a pane is not a substitute for Quit when you need a complete shutdown for updating or backup.

Quit uses a brief transition after its save and busy checks permit shutdown. If a pending save fails or an operation prevents exit, correct the problem and try Quit again; decorative motion does not override that guard.

## Expenses: records, summaries and manual order

Use **+ Expense** to enter a purchase with its name, amount, currency, spending date and category. Notes, receipt photos and reference files can provide context. Expenses represent actual recorded spending.

Choose Week, Month or Year and a currency to review totals. The chart and category shares cover the whole selected period. Search and category filtering narrow the transaction rows without changing those period-wide totals.

Open **Additional · Spending insights** for the average and largest recorded entry, days with recorded spending and top category. **Copy period summary** copies a text summary to the clipboard. The expander opens and closes smoothly; labels and feedback wrap in compact layouts.

### Reorder transactions

Drag a row's name or other non-button body area toward another transaction. Place it above or below the target, then release. The dragged row lifts with its original contour and content, while neighboring rows make room. A soft shadow distinguishes the picked-up row. Press Escape before dropping to cancel.

The order is saved for display. It does not change dates, amounts, currencies, payment links or financial history. Charts still use the recorded dates. Search, category, period and currency changes do not erase the order of records hidden by those filters.

Photos, Files, Edit and Remove/Undo paid remain action controls. Begin a reorder from the row body rather than those buttons.

## Subscriptions: forecasts and payments

Create a subscription with its amount, currency, billing interval and first due date. Upcoming dates and projected costs are schedules. They do not mean a payment has been made.

Choose **Record paid** only when you have paid an occurrence. Its saved amount, currency and paid date become a spending record. Repeating that occurrence does not create a duplicate payment. **Undo paid** reverses the active payment and retains the change in history.

**Archive** pauses future forecasting for a subscription while keeping its history. **Restore** resumes the current schedule. Archiving in Tally does not cancel a service with its provider.

The active Subscriptions list supports saved drag order. Drag the non-button row body, release before/after another row, or press Escape to cancel. Search-hidden subscriptions remain in the complete saved ordering. Reordering does not change billing dates, forecast calculations or payment history.

Currencies remain separate throughout Tally; no exchange-rate download or automatic conversion combines them.

## Daily: capture and complete tasks

Daily offers Today and Tasks, optional due dates, completion/reopen actions and archive visibility. Today distinguishes open, due-today and overdue tasks. Its progress reflects the recorded tasks due by today, rather than an invented score for an empty list.

The optional seven-day view groups tasks by their due date. It does not claim to be a history of when you completed them.

Use the available appearance and density controls when helpful. Deletion is separate from completion or archive and requires confirmation plus recovery protection. Task actions do not write financial spending or mark a subscription as paid.

The widget's Daily mode provides quick capture and a short task preview. Use **Open full Daily** for the complete workspace.

## Notes: documents, folders and actions

Open multiple documents in tabs, search the library and create folders explicitly. **Move** provides a destination picker when you prefer it to dragging. The library only realizes a bounded visible portion of a large list; search, scrolling and export still address the saved collection.

### Export or delete from a row or tab

Right-click a note in the library or its top document tab to open:

- **Export note as TXT…**
- **Export note as Markdown…**
- **Delete note…**

The tab menu also opens from its title, blank padding or close-button area, and through Shift+F10 on the focused tab control. Opening the menu alone preserves the active editor. Choosing an action targets the note whose menu you opened.

Ordinary left-click **X** closes a document tab. It does not delete the saved note. Delete requires explicit confirmation and recovery protection. A failed save keeps the draft open instead of silently discarding its text.

### Reorder, move or group notes

| Where you drop | Meaning |
| --- | --- |
| Near the top/bottom edge of another note in the same folder | Reorder those library notes. |
| In the center of another note | Offer the existing named-folder creation flow. |
| On an existing folder | Move the note to that folder. |

Use the target's narrow top or bottom edge for reordering; its center has a different purpose. The lifted note keeps its original rounded contour and content, and moving neighbors indicate insertion. Escape cancels a drag without saving a new order. Reordering changes display metadata, not document text, folder membership or document-tab order.

For a keyboard alternative, focus a library note and use **Ctrl+Shift+Up/Down** to move it among the visible notes in the same folder.

### Exchange text and reference files

Import real TXT or Markdown files to create local Notes. A note can export individually as TXT/Markdown; folder and all-note exports produce ZIPs of text documents. TXT preserves the saved body, while Markdown includes a document heading and body.

Markdown file support is not a live Markdown renderer or an external-plugin system. An Obsidian deep link is not the contents of a Markdown file; select the actual file when prompted.

Reference attachments are managed local copies. Note-text ZIPs do not include everything required for a complete profile recovery.

## Collections and local attachments

Collections supports Lists, Wishlist, Goals and Waiting On. Mark an item Done, Acquired, Reached or Resolved according to its purpose. Add details, a web reference or an optional review date, choose an icon/photo icon and attach useful files.

These completion actions do not create purchases or financial transactions. Archive keeps a collection available to restore. Delete is explicit, confirmation-protected and available for archived collections too.

The shared attachment manager supports safe images, PDF, text/Markdown/CSV and validated Office document containers. Adding a file copies it into managed storage without deleting the original. Open files explicitly or export copies individually/as ZIP. Keep the managed copies and their metadata in your profile backup.

Images stay within the rounded edges of attachment thumbnails, Collection photo icons and entry covers.

## Widget, motion and notices

Money mode shows recorded spending with Week/Month/Year recent activity and optional category/upcoming details. Daily offers tasks and quick capture. Quick Note is a separate scratchpad; Manage provides the existing expense/subscription editors without requiring a large workspace.

Money/Daily and recent-period changes use horizontal transitions. Money/Daily also has one moving selection highlight behind stable labels. Notes action menus, lifted drag previews, chart/progress reveals and insight expansion use the same brief motion style. The selected view, commands and numeric values update immediately. Motion does not move native window geometry or rewrite financial values.

Command-result notices appear, remain briefly, then dismiss automatically, including unsuccessful command results. A newer command replaces the older notice and gets its own display interval. Dismissal is visual: it does not convert failure into success or discard an unsaved draft. Validation, blocked refresh and unsaved-state explanations remain visible until addressed. Resolve the relevant field, save or recovery condition before retrying a blocked action.

Windows animation and high-contrast policy govern decorative motion. With motion suppressed, controls reach the same final state immediately. This policy is not a claim that every accessibility or monitor combination has been qualified.

## Back up and update

1. Choose **Quit Tally**, then confirm the application has exited.
2. Back up the entire selected profile. The included **Backup-Tally.ps1** refuses live-profile copies and verifies the archive it creates.
3. Run the newer Setup over the existing installation to update app files in place; its AppId, install directory and shortcut profile remain stable. For portable, replace program files without overwriting the data directory.
4. Reopen the same profile and verify your records.

Include all SQLite databases and WAL/SHM sidecars, Notes/tasks/Collections, receipts, attachments, icons, wallpaper copies, preferences and recovery files. A single database copy, note export or source Git bundle is not a complete personal backup. Do not merge independently edited profiles.

Setup is configured to retain its separate per-user data folder on uninstall; fresh install/uninstall execution is **NOT_RUN**. A private development recovery ZIP contains source/history and verified programs, but deliberately excludes personal profiles. Never publish either kind of private backup.

## Troubleshooting and reporting

- **Navigation disappeared:** use Workspace's recall action. Use Join only when you want to combine the cards.
- **Workspace disappeared:** choose a navigation item or open Tally from the widget/tray.
- **A note drag offers a folder dialog:** you dropped in the center; cancel it and use the top/bottom edge for same-folder order.
- **A save result faded:** inspect the current record/draft and any relevant validation state; notification expiry does not undo or guarantee a save.
- **Unexpected profile:** check the active path in Settings & help and the edition/shortcut used.
- **Window too large:** Windows scaling affects physical pixels; the normal default is 1040 × 700 logical units. Compact navigation stays reachable through its scrolling regions.
- **Publisher warning:** this is an unsigned preview. Check the official release hashes and keep security protections enabled.

Report the exact version, Windows/display scale, theme and reproduction steps with a redacted screenshot. Do not attach profiles, receipts, private notes, tokens or recovery ZIPs.

## Release verification and scope

**Version 0.5.11-preview.36 · 2026-11-09 · Windows x64**

| Evidence | Result |
| --- | --- |
| Full WPF application checks | **1,808 passed**; zero binding errors |
| Window geometry checks | **86 passed** |
| Focused Navigation transition | **28 passed** |
| Exact candidate and installed native checks | **20 / 20 passed**, synthetic data |
| Tally.dll SHA256 | **08E24C61D09A1C95E978E2F6190DE7C71103B4A07E4CC18B48EF54E1222C45A2** |
| Existing local Setup upgrade | Exit 0; program/data preservation verified |
| New public Setup | Same stable AppId and data path; compile/static checks only; execution/uninstall **NOT_RUN** |
| Public Portable ZIP | Extracted; every file hash matched |

These checks cover the recorded environment and selected native states, not all display hardware or every animation frame. The separately compiled public Setup was not used to update the personal installation.
Results apply to the recorded scenarios and exact release program set. Other Windows versions, GPUs, physical mixed-DPI monitor arrangements, complete accessibility coverage and long-running environmental behavior are not certified by these checks. Compilation and static inspection are not fresh installer execution.
