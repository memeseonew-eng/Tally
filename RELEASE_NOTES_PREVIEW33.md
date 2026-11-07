# Tally 0.5.11-preview.33

**Preview33 · 2026-11-07 · Windows x64 · Unsigned prerelease**

Changes since [0.5.11-preview.27](https://github.com/memeseonew-eng/Tally/releases/tag/v0.5.11-preview.27). Earlier release notes and assets remain available.

[Download and overview](README.md) · [Usage guide](USAGE.md)

## A more consistent everyday workspace

Preview33 brings together improvements to pane behavior, compact layouts, large Notes libraries, note actions and interaction feedback. Expenses, subscriptions, Daily tasks, Notes and Collections retain their local data model and existing separation: a scheduled bill is not a recorded payment, task completion is not spending, and currencies are not silently converted.

## Pane behavior and readable controls

The separated Navigation X now hides Navigation rather than joining the cards. A small recall action in Workspace brings the same pane back at its saved position. Explicit Join or deliberate edge joining remains the way to combine the panes.

Hidden Navigation and recall behavior persist through restart. Workspace hiding/reopening, saved placement and the existing minimize/restore behavior remain part of the workspace flow.

Shared popup exterior shadows were removed, and Notes text formatting was corrected for the observed missing Korean strokes. This preserves the embedded font and document text.

## Clearer actions and input states

Money/Daily and widget-period controls use consistent inset shapes and readable selection text. Empty date-field prompts no longer sit behind the caret while editing.

Notes library rows gained the same TXT export, Markdown export and guarded Delete actions as the document menu. Right-click or keyboard context-menu access targets the selected row's note identity.

Collections gained explicit recovery-protected Delete, including archived collections. Confirmed deletion checks the relevant revisions and retains attachment sidecars for recovery; cancellation preserves the records.

## Compact-window and release-process corrections

Currency control focus/open treatment and narrow finance-header layout were corrected. Initial window fitting better respects small work areas.

The development build path was tightened so publishing uses a fresh gated candidate, while activation checks both version and binary identity. These safeguards do not by themselves prove installer execution or every physical display configuration.

The broader audit recorded open environment/input and qualification limits. Later fixes below address specific findings; they do not imply that all intermittent behavior is eliminated.

## Large Notes libraries and compact navigation

The Notes library uses data-backed recycling virtualization, limiting the number of realized row controls to the visible area and its cache. Notes remain reachable through scrolling, search and export.

Compact Navigation gives the library routes usable space while optional settings/widget/status sections scroll when needed. Quit remains reachable. The normal design, fonts and caption-grab geometry are preserved.

Earlier fixture timings are not presented as performance measurements for this release.

## Note actions directly on document tabs

Top document tabs now expose **Export note as TXT**, **Export note as Markdown** and **Delete note** through right-click on the title, padding or X area, plus Shift+F10 on a focused tab control.

Opening an inactive tab's menu preserves the active editor. Actions capture the menu's original note identity, including after tab rebuilding. Existing save, confirmation, revision and recovery checks remain in the action path.

Ordinary left-click X closes the tab only. A failed save keeps the draft open, and Delete remains separate from closing.

## Motion, display order and feedback

### Notes and list dragging

Notes action menus receive a brief entrance transition. During dragging, the picked-up row lifts and visible neighbors move to show insertion without moving the original hit targets.

For Notes, drop near the **top or bottom edge of another note in the same folder** to change library order. The center keeps the existing folder-creation flow; dropping on a folder keeps the existing move action. Escape cancels without saving order. Ctrl+Shift+Up/Down offers a keyboard alternative among visible same-folder notes.

Transactions and active Subscriptions gain the same saved display-order interaction. Drag the row body rather than action buttons. Filtering, currency or period changes preserve hidden records in the saved full ordering.

Ordering is presentation metadata. It does not change financial dates, amounts, payment provenance, history, forecasts or chronological chart calculations.

### Rounded drag previews and pictures

The lifted row keeps its original contour, content scale and any existing outline, with a soft shadow to convey the lift. The extra outer frame and pale corner fill observed when dragging Notes have been removed. The shared correction applies to the drag previews used by Daily tasks, Transactions, Subscriptions and Collections.

Attachment thumbnails and Collection photo icons in the sidebar, header and editor now contain pictures within their rounded edges. The same correction applies to Collection entry covers. Their existing dimensions and the attachment thumbnail background are preserved.

### Widget and data visuals

Money/Daily and Week/Month/Year changes receive horizontal transitions. Money/Daily keeps one sliding selection highlight behind stable text during hover and press, eliminating the overlapping capsules during mode changes. Values, selection state and commands update immediately, including during rapid reversal.

Recorded-spending chart bars, category shares and Daily progress receive short visual transitions. **Additional · Spending insights** expands/collapses smoothly and wraps text/feedback in compact layouts.

Decorative animation leaves native window bounds and recorded values unchanged. System animation/high-contrast policy controls motion; reduced motion reaches the same final state without the decorative transition.

### Notices and guarded Quit

Command-result notices reveal, remain briefly and dismiss automatically, including unsuccessful command results. Repeating or replacing a command result restarts the appropriate notice lifetime rather than letting an obsolete callback hide a newer message.

Validation, blocked refresh and unsaved-state explanations remain visible until addressed.

Notice dismissal is presentation only. It does not discard a draft, remove save protection, acknowledge a destructive confirmation or turn a failed operation into a successful one.

Quit receives a brief exit transition only after pending-save and busy checks allow shutdown. A blocked save or operation still prevents exit.

## Installation and updating

The public deliverables are a Windows x64 portable ZIP, per-user Setup EXE and **SHA256SUMS.txt**. Both editions include self-contained .NET and Windows Desktop runtime **10.0.14**.

Portable data lives beside Tally.exe in **data/**. Setup shortcuts select **%LOCALAPPDATA%\Tally\data**. The profiles are separate and are not automatically imported or merged.

Before updating, choose **Quit Tally**, back up the entire current profile and replace program files only. Preserve all SQLite sidecars, optional-module databases, notes, attachments, receipts, icons, wallpaper copies, settings and recovery files.

A developer/source recovery ZIP is private and does not contain personal profiles. It must never be attached to this public release.

## Release verification and scope

**Version 0.5.11-preview.33 · 2026-11-07 · Windows x64**

| Evidence | Result |
| --- | --- |
| Automated WPF application checks | 1,635 passed; zero binding errors |
| Native widget, menu, notice, insights and Quit checks | 10 passed |
| Native pointer reorder, cancellation and restart checks | 17 passed |
| Application DLL SHA256 | `459A6F484FF9998319FB85EBD453AFF5B0D99DF459538B40E46F0B2090582FA4` |
| Recorded native environment | Current Windows 11 x64 device, 96 DPI (100% scaling). |
| Setup qualification | Compilation and static package/retention checks only. Fresh install/uninstall execution: **NOT_RUN**. |

Native Quit checks confirm guarded exit. PrintWindow captures do not certify the full compositor fade or exact visual timing.

Results apply to the recorded scenarios and exact release program set. Other Windows versions, GPUs, physical mixed-DPI monitor arrangements, complete accessibility coverage and long-running environmental behavior are not certified by these checks. Compilation and static inspection are not fresh installer execution.

## Remaining boundaries

This remains an unsigned prerelease. Verify official release checksums and keep Windows security protections enabled.

Qualification is bounded to recorded devices and scenarios. Other Windows versions, GPUs, physical mixed-DPI layouts, complete accessibility coverage, clean-machine installation and long-run environmental behavior require their own evidence. Existing intermittent-input limitations must remain explicit where unresolved.

There is no bank connection, automatic currency conversion, built-in cloud synchronization, external plugin marketplace or public automation API. Stock charts remain research, not a shipped feature.

The public repository contains documentation, metadata, synthetic screenshots and binary downloads. Private application sources, WPF resources and development Git history remain private. Report problems with a version, display scale and reproducible steps; never include personal profiles, notes, receipts, credentials or private recovery archives.
