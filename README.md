# Releases Notes

Neevis v1.11.1

## Changes
1- **About / Support:** Added separate **Report Issue** and **Send Suggestion** actions with a focused feedback form that sends the user's title, description, selected Neevis area, and safe product/support metadata without arbitrary file attachments.
2- **Reliability / Diagnostics:** Added protected background client-report handling for user feedback and observed Neevis-owned managed failures, including local retry when a report cannot be delivered immediately. Reporting remains independent from normal product operation.
3- **Usage Statistics:** Separated application-session duration from tool-backed usage totals so cumulative total usage reflects recorded Neevis tool execution time rather than time the host application remains open.

## Fixes
1- **Analyzer:** When Analyzer updates selected or Workspace Clash Tests, the loading screen now shows the current Navisworks model name so the active update target is clear.

## Known Issues
1- **Portal:** Switch Back remains under observation until confirmed stable on representative central/workshared models.
2- **Clashes Data Transfer / Sync Data:** Large real-project datasets should continue to be used to validate import/apply and synchronization performance; no fixed performance multiplier is claimed.
3- **Hotkeys:** Switch Select Mode still requires Navisworks host confirmation of the previously reported failing scenario.
