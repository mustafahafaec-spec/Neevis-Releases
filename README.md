# Neevis (Latest Version v1.9.7)

**Neevis** is a productivity add-in for Autodesk Navisworks Manage 2026 and 2027. It provides Workspace-based clash analysis, Search Set authoring, clash-management and review workflows, reporting, saved-viewpoint tools, model-finding utilities, geometry export, hotkeys, and coordination tools.

> **BETA tools/features:** Search Set Builder, Workspace, Clashes Data Transfer, Right Click Options, and the Viewpoints portion of Sync Data remain under wider testing.
>
> **Coming Soon:** Stamper, Reporter Create View Points, and Reporter image export are **ALPHA** and are not executable in the v1.9.7 Public Release.

## Main Tools

### Tests and Sets

- **Matrix to Tests** creates clash tests from an Excel matrix.
- **Tests Editor** exports clash-test settings to Excel and applies controlled edits back to Navisworks. Supported built-in and discoverable custom Clash Detective rule states are available as editable YES/NO columns and participate in Excel import/export and Workspace verification/transfer when the current Navisworks model supports those rules.
- **Search Set Builder (BETA)** creates, edits, arranges, imports, exports, and synchronizes Navisworks Search Sets. It supports folders, condition editing, AND/OR/NOT logic, undo/redo, model-derived Property Set/Property/Value helpers, Selection Tree assignment, and Excel workflows.

### Workspace and Analyzer

- **Workspace (BETA)** provides the shared Neevis Workspace used by Workspace-aware tools. The central Workspace is a single portable **`.nws`** file with independently compressed and revisioned data sections. Existing **`.nat`** Workspaces can be converted to `.nws` without modifying the original `.nat` file.
- Workspace stores coordination definitions, shared settings, Analyzer records, cache-file update information, per-test clash records, clash metadata/group membership, source-file relationships, synchronized Viewpoints, and supporting cross-host identity. Clash snapshots also retain clash-side **Document > Title** ownership metadata and Analyzer **Last Recorded Current Clash Count** values for supported test/group aggregate levels so Reeviz and other consumers can use Neevis-authored coordination state directly.
- Frequent `.nws` operations use section-level and batched reads/writes so settings, recordings, Sync Data channels, Screening, and repository updates do not repeatedly materialize unrelated Workspace data.
- **Workspace Tests Update Rules** determine when a Workspace-aware Clash Test requires rerunning: reset/not-run state, a recorded live-clash-count mismatch, or a relevant cache update newer than the test's last run.
- Opening Workspace-aware tools no longer waits for a monolithic verification pass. Fresh verification proceeds cooperatively in the Navisworks host context after the tool opens and now publishes completion immediately to open Workspace UI, while explicit **Sync Data** and manual **Verify** remain synchronous authoritative boundaries.
- **Analyzer** provides Workspace-based clash analysis with Items, Groups, Combo Groups, Main Groups, recorded clash history, Clash Summary, Clashes Table, **Clashes Matrix**, Priority Items, Clashes Timeline, reporting, and model isolation.
- Analyzer updates only Workspace tests that currently require an update. Before running them, Neevis unhides the Search Set content associated with the affected Workspace Items, runs the required tests, restores the prior hidden state, and refreshes only the affected Workspace clash records.
- Analyzer **General settings are local per user/machine**. Workspace-specific definitions and records remain Workspace data.
- Analyzer recording never starts Clash Test updates automatically. If relevant Workspace tests require updating, Record is blocked and the user is instructed to run **Update Workspace Tests** first. In the Clashes Table, Difference compares the latest two saved records when two or more exist; with one saved record it compares that record against the current reading.
- Analyzer isolation follows the statuses selected under **Statuses included in Total**; clashes moved to excluded statuses are removed from the active isolated clash view.
- **Universal Clash Capture Settings** controls clash-isolation/capture appearance consistently across supported Neevis workflows.
- **Viewpoint Manager** organizes saved viewpoints, supports comments and Navisworks text markups, exports and updates Excel reports with images, and exchanges viewpoint XML files.

### Centralization and Clash Coordination

- **Sync Data** is the explicit central synchronization workflow. It saves the current NWF first, performs authoritative Workspace verification, then synchronizes the data types selected by the user. The user's selections are remembered for the next Sync Data session.
- Sync Data uses persistent per-test and per-clash change tracking, Workspace change journals, and exact repository patching so Clash Data, Clash Groups, and the authoritative Workspace clash repository process only the affected data when the synchronization state can be proven. Bounded journal gaps are reconstructed from current Workspace snapshots when safe, while conservative authoritative fallbacks remain for genuinely unknown or structural state.
- Sync Data presents independent progress stages for **Saving the current file**, **Workspace verification**, and each selected data channel, and shows the total elapsed synchronization time while the operation is running.
- **Clashes Data Transfer (BETA)** exchanges selected clash metadata between the model and Workspace. Reviewed and Approved are the synchronized review-status scope; metadata fields include Priority, Description, Comments, Assigned To, and Approved By. Central reconciliation remains field-aware and change-driven.
- **Clash Groups** is an independent, setting-free Sync Data channel. Group membership is synchronized separately from clash metadata/status and is independent of clash review status.
- **Sync Data – Viewpoints (BETA)** synchronizes Workspace Saved Viewpoints, folders, and supported saved visibility/appearance attributes between verified models. Native Navisworks Viewpoints XML is used as the normal camera/tree transfer path, while Neevis preserves the synchronized camera when receiver-side saved attributes must be recaptured.
- **Clash Grouper** groups clashes using user-defined grouping criteria with optimized startup/property discovery for larger coordination models.
- **Right Click Options (BETA)** adds Neevis actions to the Navisworks selection context menu, including clash isolation, grouping/report access, review/approve related clashes, IFC export, and view reset actions.

### File and Model Utilities

- **File Manager** lists loaded Navisworks cache/model files with source information, paths, and update dates, and supports multi-selection removal/repath-related workflows.
- **Purger** removes selected categories of saved Navisworks model data.
- **Get Revit ID** copies Revit Element IDs from selected Navisworks objects.
- **By Revit ID** locates model objects using Revit Element IDs.
- **Hotkeys** assigns two-key shortcuts to Neevis tools and supported native Navisworks commands. Hotkeys are suppressed while Navisworks Sets/Search Sets/Selection Sets owns keyboard focus so native folder renaming does not trigger Neevis commands.

### Exporting and Reporting

- **Results Count** exports clash-result counts as a table or as a Search Set matrix.
- **Reporter** creates configurable HTML clash reports with selectable fields, statuses, comments, grouping, filters, and split-report options. **Create View Points is ALPHA / Coming Soon** and is unavailable in the Public Release.
- **Reporter image export is ALPHA / Coming Soon** and is unavailable in the Public Release.
- **NaviSolid** exports selected Navisworks geometry to DWG and transfers geometry to an opened AutoCAD drawing.
- **IFC Export** exports Navisworks geometry to IFC4. The main workflow lets the user choose export content from the Selection Tree, while the Right Click Options shortcut exports the current selection directly.

### Settings and Updates

- **About** provides version, appearance, licensing, update controls, Auto Update, update-notification preferences, Universal Clash Capture Settings, and bug/suggestion reporting.
- Neevis settings can be exported and loaded from About for supported tools, allowing user preferences to be transferred between installations.

### Coming Soon

- **Stamper (ALPHA)** remains visible as an under-development tool but does not execute in the v1.9.7 Public Release.
- **Reporter Create View Points (ALPHA)** remains visible as Coming Soon and does not execute in the Public Release.
- **Reporter Images (ALPHA)** remains visible as Coming Soon and does not execute in the Public Release.

## v1.9.7 Highlights

- Adds an **Only Updated Tests** Sync Data run mode that synchronizes only relevant Clash Tests already considered current, without running or updating tests during that mode.
- Extends Workspace cross-host Item metadata with **Main Documents**, using unique `Document > Title` values across Item elements and falling back to `Item > Source File` where required.
- Strengthens Clash Groups synchronization so central group membership remains authoritative across group moves and Clash Test reset/rerun recovery, while keeping the group channel separate from clash review metadata.
- Improves Sync Data review/status handling for Navisworks test states reported as either **Done** or **Complete**, and tightens Reviewed/Approved transfer targeting.
- Prevents broad Clash Group recovery candidates from automatically forcing full Workspace clash indexing; repository refresh is now limited to tests with actual group-membership consequences.
- Retains the section-level `.nws` I/O and delta-tracking architecture while continuing performance and synchronization reliability work for large coordination Workspaces.

## Known Issues

1. **Sync Data reliability:** Synchronization is still not fully reliable, and multiple Workspace data types may fail to transfer between models/users as expected. This is a known issue and will be addressed in an upcoming public patch release.
2. **Sync Data performance:** Large or structurally changed Workspaces can still require conservative Navisworks reconciliation, so very large-model synchronization performance remains under real-project validation.
3. **Sync Data – Viewpoints (BETA):** Saved Viewpoints containing saved visibility/appearance attributes can still take significantly longer to synchronize and may cause noticeable latency on large models.

## Compatibility

- Autodesk Navisworks Manage 2026
- Autodesk Navisworks Manage 2027
- Windows x64
- .NET Framework 4.8
- AutoCAD is required for NaviSolid DWG export and transfer to an opened AutoCAD drawing.

## Current Testing / Coming Soon

- **Search Set Builder — BETA**
- **Workspace — BETA**
- **Clashes Data Transfer — BETA**
- **Right Click Options — BETA**
- **Sync Data Viewpoints — BETA**
- **Reporter Create View Points — ALPHA / Coming Soon**
- **Stamper — ALPHA / Coming Soon**
- **Reporter Images — ALPHA / Coming Soon**

## Future Plans

- Resolve the remaining Sync Data transfer-reliability issues in an upcoming public patch release.
- Continue validation and performance work for BETA Saved Viewpoint synchronization on large federated models.
- Continue validation of BETA workflows based on project use and tester feedback.
- Continue Stamper development before enabling it in a future Public Release.
- Continue development of Reporter Create View Points and image export before enabling them in a future Public Release.
- Expand Workspace-based interoperability with Reeviz and other coordination workflows.

## Author

Developed by Mustafa Hesham.
