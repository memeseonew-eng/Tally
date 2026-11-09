# Tally 0.5.11-preview.36

**Preview36 · November 9, 2026 · Windows x64 · Unsigned prerelease**

This release updates the public Preview33 application with the accepted UI25–UI27 refinements. The entire product remains local-first: there is no required account, online banking connection, automatic exchange-rate conversion, external plugin system, or cloud synchronization.

[Overview and downloads](README.md) · [Complete usage guide](USAGE.md) · [Previous Preview33](RELEASE_NOTES_PREVIEW33.md)

## What changed after Preview33

### A softer desktop widget, without an interface redesign

The compact widget keeps its Money, Daily, Quick Note and Manage flows. Its surfaces now use a more restrained iPadOS/iOS-inspired glass treatment: a soft perimeter, subtle reflection, inset inner surface and clear, independent foreground text. Both light and dark appearances were reviewed; glass does not blur the words, amounts or controls.

The outer corner shape has been brought closer to the rest of the workspace. It includes an inset surface and the familiar two-line bottom-right resize grip, replacing the detached-looking triangular cue. Existing size limits, position memory, locking and the Open Tally click target remain. Hover and selected states do not create a second selection highlight during Money/Daily transitions.

Small text buttons, including View expenses, use less exaggerated corner rounding and safer internal padding so labels do not press against rounded ends.

### Start with Windows is now optional

Settings includes a single **Start with Windows** switch. When enabled, Tally registers its own installed executable and profile for Windows sign-in; when disabled, it removes its recognized registration. Opening Settings does not silently enable startup.

The installer and uninstall logic distinguish Tally's own registration from a foreign or manually modified startup entry. A new Setup does not turn the option on just because it is installed. An existing user's setting is preserved by a normal upgrade.

This feature is **not an automatic version updater**. Tally does not download or install future releases without the user choosing to run a newer Setup.

### Sharper Notes opening and a less crowded library

Notes now presents its initial document text at full opacity instead of allowing two first-open reveal paths to make it look temporarily washed out. Deliberately switching between documents still uses the existing transition.

The Notes library column is slightly narrower: **226 → 210 DIPs**, giving the editor more horizontal room without replacing its structure. Longer note names use a bounded, single-line ellipsis rather than ending abruptly in the middle of a glyph. Full titles remain intact in the stored note, tooltip and accessibility name.

The large-library recycling and virtualization introduced earlier remain. The library's search, folder controls, bottom actions, drag ordering and document tabs remain in place.

### The Navigation restore control exits naturally

When a separated Navigation card has been hidden, Workspace shows the small Navigation recall action. Pressing it restores the **same** Navigation card at the remembered position. The recall control now fades away and moves upward a few pixels during a **160 ms** exit instead of vanishing abruptly.

Rapid repeat interactions and mid-transition reversals continue from the currently rendered state rather than restarting at full opacity. The control stops accepting pointer input immediately when hiding. The pane's native position and dimensions are not animated.

The small Navigation **X still hides/closes that card**. It does not join the windows. Join remains an explicit, separate action.

## Major features in Tally

### Expenses: recorded spending, not estimates

Record expenses with an amount, currency, date, category and optional notes or reference attachments. Choose Week, Month or Year to inspect the corresponding spending chart and category distribution. Search and filter the transaction list without changing the full period's displayed totals.

Open **Additional · Spending insights** for extra summary measures; expand and collapse it with the existing brief animation. The transaction list supports lifted-row drag reordering that persists across restart without changing the underlying financial dates, amounts or chart calculations.

Tally does **not** blend currencies using unstated rates. Scheduled subscriptions are forecasts until a payment is explicitly recorded.

### Subscriptions: recurring costs and actual payments

Create recurring entries with dates, currencies, billing cycles and categories. See upcoming commitments and estimated future costs. Record a payment with **Record paid** only when it happened; the linked expense and the saved payment snapshot then reflect the actual occurrence. **Undo paid** reverses the active settlement while keeping relevant history.

Archive and restore recurring entries without treating an archive command as a real-world cancellation. The list supports saved display ordering. Destructive removal requires explicit confirmation and a successful recovery snapshot.

### Daily: tasks, due dates and progress

Create tasks, optionally give them due dates, mark them complete, reopen them and archive them. Today emphasizes due and overdue work. The progress bar animates when its state changes, while the underlying count remains exact. The widget's Daily mode offers quick capture and concise task previews.

Task completion is separate from recorded expenses and subscription payments.

### Notes: documents, folders and export

Keep multiple documents open in top tabs; search a large local library and organize documents with folders. Drag notes to existing folders, drop at a neighboring note's edge to reorder within a folder, or use the existing keyboard alternative.

Right-click a library note or its document tab for **Export as TXT**, **Export as Markdown** and **Delete**. The ordinary tab X closes a tab, not the document. Deletion requires confirmation and recovery protection, including for unsaved changes.

Import TXT and Markdown files and export individual documents or folders as text files. Reference attachments stay in managed local storage. This is not a live Markdown renderer or a native Obsidian sync system.

### Collections: useful lists and attachments

Create Lists, Wishlists, Goals and Waiting On collections with distinct completion states. Add notes, reference links, check dates and local file attachments; choose an icon or photo. Archive or restore a collection; deletion requires confirmation and recovery protection.

Images in collection covers, photo icons and attachment thumbnails stay within their rounded surfaces.

### Widget, customizable workspace and motion

Switch between the compact widget and full workspace. Keep the widget visible or use the system tray; close the app completely with Quit Tally. Configure available appearance, local wallpaper, theme, density and optional widget details without adding a separate cloud account.

Separate Navigation and Workspace into movable, resizable cards and restore their saved placement. Notifications for command results arrive and automatically dismiss after a short interval; persistent validation errors remain until addressed. Chart, task progress, mode transitions, menu opening, list dragging and guarded Quit share brief, restrained animation. A failed save still blocks a destructive action or exit.

## Download and upgrade

The release provides **two executable editions** and a **SHA256SUMS.txt** file:

- **Windows Setup** installs per-user under %LOCALAPPDATA%\Programs\Tally. It uses the stable Tally AppId across releases. Running the newer Setup over an existing Setup installation upgrades application files in place while the shortcuts retain **%LOCALAPPDATA%\Tally\data**. The installed profile is deliberately outside the replaceable program directory.
- **Portable ZIP** should be extracted into a writable folder. Launch Tally.exe or Open-Full-Tally.cmd. Its **data/** folder beside the executable is separate from the Setup profile.

**Upgrade steps:** choose **Quit Tally** (hiding the widget alone is not enough); back up the complete active data profile; download and run the new Setup; open Tally from the existing shortcut and check that the same records appear. Do not overwrite the data directory with an empty copy and do not merge independently edited profiles.

The per-user Setup upgrade mechanism was exercised on this machine across previous local previews, including Preview35 → Preview36; this public Setup was separately compiled from the same verified application runtime and installer identity. **A fresh-machine install/uninstall and execution of this separately compiled public Setup were not run**. The portable ZIP was extracted and compared file by file.

Both editions bundle .NET and Windows Desktop runtime **10.0.14**. No separate .NET installation is needed. Tally is unsigned; Windows may display a publisher warning. Verify the download checksum and keep your Windows protections enabled.

## What is—and is not—backed up

A complete **personal profile backup** includes all relevant SQLite databases and sidecars, Notes, Tasks, Collections, receipts and attachments, icons, wallpaper copies, preferences and recovery snapshots. The included Backup-Tally.ps1 helper refuses a live-profile copy.

A **developer recovery archive** is different: it contains private code, Git history, accepted binaries and build/verification evidence but intentionally **does not contain personal financial records or Notes**. It is never distributed through this public release.

Tally does not automatically sync your profile to the cloud. Portable and Setup profiles are not imported or merged automatically.

## Verification summary

| Check | Accepted result |
| --- | --- |
| Exact application binary | **Tally.dll SHA256: 08E24C61D09A1C95E978E2F6190DE7C71103B4A07E4CC18B48EF54E1222C45A2** |
| Official build | Zero warnings, zero errors |
| Core and storage | 53 + 61 checks passed |
| Daily/Collections, fault and architecture | 104 + 35 + 15 checks passed |
| Full WPF regression | **1,808 checks passed**, zero binding errors |
| Pane/window geometry | **86 checks passed** |
| Focused Navigation transition | **28 checks passed**; sampled fade/reversal values |
| Native candidate and installed runtime | **20 / 20 checks passed**, using synthetic data |
| Private installed Setup upgrade | Exit 0; 487 packaged files matched; 64 personal files unchanged against the guarded pre-install snapshot |
| Public installer | Separate compile and package checks; **direct install/uninstall NOT_RUN** |
| Public portable ZIP | Complete extraction and file-hash comparison |

All test counts refer to the recorded runs and scenarios, not a promise of universal hardware compatibility. Four settled images per runtime were reviewed, but sparse screenshots alone do not certify the complete native animation timing. OS animation-off/high-contrast execution, actual new-machine installation/uninstallation, Windows reboot/sign-in and physical mixed-DPI monitors remain **NOT_RUN**.

## Scope and privacy

The public repository holds feature explanations, synthetic screenshots, download files and release metadata. It does not expose the private application source repository or Git history. No personal records, receipts, Notes or developer recovery ZIP are public release assets.

Please report reproducible bugs with the version, Windows version, display scaling, theme and steps. Never attach your complete private profile or source recovery archive to an issue.

**Planned, not shipped:** stock charts and external plugins. Bank integration and automatic currency conversion are not provided.
