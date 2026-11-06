# Tally 0.5.11 Preview 27 — Motion that remembers your workspace

This update completes the shared minimize/restore animation and qualifies the previously pending window-placement memory work. The basic interface remains uncluttered; no extra animation switch or stock-chart module is added.

## Download

- [Portable ZIP — Windows x64](https://github.com/memeseonew-eng/Tally/releases/download/v0.5.11-preview.27/Tally-Portable-v0.5.11-preview.27-win-x64.zip)
- [Windows Setup](https://github.com/memeseonew-eng/Tally/releases/download/v0.5.11-preview.27/Tally-Setup-v0.5.11-preview.27-win-x64.exe)
- [SHA256 checksums](https://github.com/memeseonew-eng/Tally/releases/download/v0.5.11-preview.27/SHA256SUMS.txt)

Unsigned prerelease, self-contained .NET/Windows Desktop 10.0.14 x64. Compare hashes and retain Windows security protections.

## A matching minimize and restore

Joined and detached windows now share a short, bounded contraction/fade before native minimization, with the matching reveal on restore. Native Left, Top, Width and Height do not participate in the animation. The rounded surface and remembered geometry are preserved.

Caption buttons and the Windows system minimize command use the same controller. Repeated minimize requests do not stack; restoring or closing during the outgoing transition cancels its stale completion. Minimize is blocked during modal/docking transitions. Windows animation-off and high-contrast choices are respected by the motion policy.

## Your arrangement survives restarting

Tally saves the combined window's position and size, or both cards' placement when separated. It retains navigation order, each pane's role and an intentionally hidden Workspace. Selecting a navigation item reopens that Workspace at its remembered location.

Normal geometry is saved when exiting minimized; transient animation frames are not persisted. A widget-only startup does not erase a previously stored workspace layout. Accessible partly-offscreen placement is retained, while a window stranded on a removed monitor is recovered. Placement is a separate local `workspace-layout.json`; it does not change financial records.

## Reliable full-width navigation dragging

The small card's upper blank area keeps its full width and existing vertical band. It now captures the pointer on press, before a quick movement can leave the strip, and applies the first fast movement rather than dropping it. Caption buttons retain priority and the tally wordmark remains inert.

Existing 440ms, release-only edge joining, small-X join / large-X hide, editor corners, dark fields and optional-module behavior remain intact.

## Verification

Preview27 passed the full 1,282-check WPF/UI suite with zero binding errors, 86 pane-geometry checks, 65 focused minimize checks, 53 Core, 61 Storage, 91 Daily/Collections and 15 architecture checks.

Packaged real-window testing includes 30 minimize/restore checks and 31 fast-input/process-restart checks. Additional existing native regressions cover edge docking, pane lifecycle, downward movement, resize/restore and editor/grip behavior. Verification uses synthetic profiles, not personal records.

Qualification is on the current Windows 11 x64 device. Pure geometry/raster checks are not physical mixed-monitor, other-GPU, Windows-version or comprehensive accessibility certification. Setup compilation/static retention and ZIP extraction/hash checks do not imply a fresh installation/uninstallation test.

## Updating

Use **Quit Tally**, back up the **whole** existing data folder, then replace program files only. Portable data remains beside Tally.exe; Setup uses `%LOCALAPPDATA%\Tally\data` and retains it on uninstall. Preserve database sidecars, Notes, Daily, Collections, files, wallpapers and settings. Do not merge independently edited profiles.

The in-app official download links now name Preview27 rather than the legacy Beta2 page. Updates remain manual. Previous public releases remain available for recovery.

US stock-chart integration is being evaluated separately. This release contains no quote provider, API key, chart-browser dependency, trading connection or financial advice feature.

[Full usage guide](https://github.com/memeseonew-eng/Tally/blob/main/USAGE.md) · [All versions](https://github.com/memeseonew-eng/Tally/releases)
