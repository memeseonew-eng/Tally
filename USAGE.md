# Using Tally

## Start with the right profile
The portable package starts from Tally.exe and stores data in the adjacent data/ folder. Open-Full-Tally.cmd opens the full workspace directly. Setup shortcuts use %LOCALAPPDATA%\Tally\data. The two editions do not automatically share records. The default startup is the desktop widget; open the main workspace through its Open Tally action or the tray menu.

## Windows and cards
Use the top split button to separate navigation and content. The small navigation card can also be separated from its upper blank drag strip. Grab empty upper space, not the tally wordmark. Buttons keep their own click targets. Resize separated cards at the bottom-right handle.

Small-card X rejoins; large-card X hides that workspace. Selecting a navigation row brings the workspace back, including the current row. Use Quit Tally for a complete exit. To join by proximity, align facing left/right edges, pause about 440 ms and release after the frosted cue strengthens. Retreat or Escape cancels. A quick pass or stationary adjacency cannot join by itself.

Preview25 does not remember the two separate window positions across a full process restart. The upcoming candidate is deliberately not in this public package.

## Spending and schedules
Expenses are records of actual spending. Subscription schedules are forecasts until a payment is explicitly recorded. Do not treat a forecast as a settled payment. Currency totals remain separate; Tally does not download exchange rates or silently convert currencies.

## Daily, Notes and Collections
Daily holds tasks, optional due dates, completion and archived items. Notes holds local documents, tabs, folders and reference attachments. Text/Markdown import/export does not mean the editor is a live Markdown renderer. Collections offers lists, wishlists, goals and Waiting On views. These features do not imply external plugin compatibility, AI integration or a public API.

## Back up before updating
1. Quit Tally completely through its menu/tray action.
2. Run the included Backup-Tally helper or copy the ENTIRE data folder to a private destination.
3. Verify the backup before replacing program files. Keep SQLite sidecars, documents, attachments, wallpapers, preferences and recovery copies together.
4. Update the program, then reopen the same profile. Never merge two independently edited databases.

Portable: keep the existing data/ beside Tally.exe. Setup: the installer uses the same per-user application identity; uninstall retains the separate personal data folder. A private developer/source ZIP does not contain your personal records unless its manifest explicitly says so. Do not upload profiles or developer saves to public GitHub.

## Troubleshooting
- Too large? Windows scaling changes physical window size. The default is 1040x700 logical units, around 1300x875 physical pixels at 125%. Fonts are unchanged.
- Cannot find a hidden workspace? Select a row in the remaining navigation card, or use Open Tally from the tray/widget.
- Old download page? Preview25's legacy in-app shortcut may open Beta2. Follow that page's current-release notice or use the README download buttons.
- Unsigned-publisher warning? This preview is unsigned. Check the release hashes; keep security protections enabled.
- Different result on another display? Report resolution, scale, monitor arrangement, theme, build and reproduction steps. Mixed-DPI and all GPUs/Windows versions are not comprehensively certified.

## Report a problem safely
Use Issues with a redacted screenshot and a short, repeatable sequence. Never attach the data folder, private database, receipts, full backup, recovery ZIP, access token or personal document. See SECURITY.md for security-related reports.