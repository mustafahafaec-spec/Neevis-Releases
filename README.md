# Neevis (Latest Version v1.9.3)

**Neevis** is a productivity add-in for Autodesk Navisworks Manage 2026 and 2027. It provides Workspace-based clash analysis, Search Set authoring, clash-management and review workflows, reporting, saved-viewpoint tools, model-finding utilities, geometry export, hotkeys, and coordination tools.

> **BETA tools/features:** Search Set Builder, Workspace, Clashes Data Transfer, Right Click Options, and Clash Reporter Create View Points remain under wider testing.
>
> **Coming Soon:** Stamper and Clash Reporter image export are **ALPHA** and are not executable in the v1.9.3 Public Release.

## Main Tools

### Tests and Sets

- **Matrix to Tests** creates clash tests from an Excel matrix.
- **Tests Editor** exports clash-test settings to Excel and applies controlled edits back to Navisworks. v1.9.3 adds editable YES/NO columns for supported Clash Detective rule states and includes those values in Excel import/export. See **Known Issues** for current custom-rule limitations.
- **Search Set Builder (BETA)** creates, edits, arranges, imports, exports, and synchronizes Navisworks Search Sets. It supports folders, condition editing, AND/OR/NOT logic, undo/redo, model-derived Property Set/Property/Value helpers, Selection Tree assignment, and Excel workflows.

### Workspace and Analyzer

- **Workspace (BETA)** provides the shared Neevis Workspace used by Workspace-aware tools. It supports Workspace creation/loading, verification, synchronization, screening, export, shared settings, Workspace appearance behavior, Analyzer Records, cache-file awareness, staged Model/Workspace verification repair, and supported Clash Test rule-state verification/transfer.
- **Analyzer** provides Workspace-based clash analysis with Items, Groups, Combo Groups, Main Groups, recorded clash history, Clash Summary, Clashes Table, **Clashes Matrix**, Priority Items, Clashes Timeline, reporting, and model isolation.
- Analyzer **General settings are local per user/machine**. Workspace-specific definitions and records remain Workspace data.
- Analyzer isolation follows the statuses selected under **Statuses included in Total**; clashes moved to excluded statuses are removed from the active isolated clash view.
- **Priority Items** appears before Clashes Timeline. Right-clicking an individual stacked-bar segment exposes the standard Analyzer actions for that clicked Item/counterpart scope.
- **Universal Clash Capture Settings** controls clash-isolation/capture appearance consistently across supported Neevis workflows.
- **Viewpoint Manager** organizes saved viewpoints, supports comments and Navisworks text markups, exports and updates Excel reports with images, and exchanges viewpoint XML files.

### Clash Coordination

- **Clashes Data Transfer (BETA)** exchanges selected clash metadata between the model and Workspace and supports manual/automatic synchronization using configured Clash Tests, statuses, groups, and data fields. In v1.9.3 PATCH1, Status is mandatory transfer data for enabled Reviewed/Approved/Resolved statuses; selected statuses override New/Active, selected-status conflicts use the newer change time, and ordinary fields use non-empty-first then newer-change-time matching. Signals notify Automatic Sync when shared data should be reconciled.
- **Clash Grouper** groups clashes using user-defined grouping criteria with optimized startup/property discovery for larger coordination models.
- **Right Click Options (BETA)** adds Neevis actions to the Navisworks selection context menu, including clash isolation, grouping/report access, review/approve related clashes, IFC export, and view reset actions.

### Exporting and Reporting

- **Results Count** exports clash-result counts as a table or as a Search Set matrix.
- **Clash Reporter** creates configurable HTML clash reports with selectable fields, statuses, comments, grouping, filters, and split-report options. **Create View Points remains BETA** and its loading process can be cancelled safely.
- **Clash Reporter image export is ALPHA / Coming Soon** and is unavailable in the Public Release.
- **NaviSolid** exports selected Navisworks geometry to DWG and transfers geometry to an opened AutoCAD drawing.
- **IFC Export** exports Navisworks geometry to IFC4. The main workflow lets the user choose export content from the Selection Tree, while the Right Click Options shortcut exports the current selection directly.

### Utility Tools

- **Get Revit ID** copies Revit Element IDs from selected Navisworks objects.
- **By Revit ID** locates model objects using Revit Element IDs.
- **Hotkeys** assigns two-key shortcuts to Neevis tools and supported native Navisworks commands. Hotkeys are suppressed while Navisworks Sets/Search Sets/Selection Sets owns keyboard focus so native folder renaming does not trigger Neevis commands.
- **About** provides version, appearance, licensing, update controls, Auto Update, update-notification preferences, Universal Clash Capture Settings, and bug/suggestion reporting.

### Coming Soon

- **Stamper (ALPHA)** remains visible as an under-development tool but does not execute in the v1.9.3 Public Release.
- **Clash Reporter Images (ALPHA)** remains visible as Coming Soon and does not execute in the Public Release.

## v1.9.3 PATCH1

- Reworks **Clashes Data Transfer (BETA)** Automatic Sync into field-level matching rather than whole-clash last-change-wins.
- Removes **Status** from optional Data Fields; Status is always transferred for enabled Reviewed/Approved/Resolved status scope.
- A synchronized Reviewed/Approved/Resolved status always overrides New/Active. Conflicts between synchronized statuses use the newer status-change signal time.
- For other synchronized fields, a populated value always overrides an empty value; when both sides contain values, the newer field-change signal time wins.
- Unchecked Reviewed/Approved/Resolved statuses pause synchronization for those states on that model without erasing the shared Workspace state.
- Manual Model → Workspace synchronization now writes through the same field-level signal/conflict engine, so it follows the same status and data-field rules and directly notifies Automatic Sync models.

## v1.9.3 Highlights

- Adds supported Clash Detective rule-state columns to Tests Editor with YES/NO editing and Excel round-trip support.
- Adds supported Clash Test rule-state verification and Model ↔ Workspace transfer to Workspace Verification.
- Adds Analyzer context actions directly to Priority Items stacked-bar segments and moves Priority Items before Clashes Timeline.
- Makes Clashes Data Transfer Automatic Sync apply pending Workspace-side changes back into the model automatically.
- Reduces Analyzer opening delay and Workspace Clash Test definition-reading overhead.
- Fixes Priority Items context-menu host instability and improves Clashes Matrix toolbar/merged-label rendering.
- Extends Hotkey suppression to native Sets/Search Sets/Selection Sets keyboard focus.

## Known Issues

1. **Tests Editor:** Custom-made Clash Detective rules do not appear in the Tests Editor table.
2. **Workspace Verification (BETA):** Custom-made Clash Detective rule states do not affect Workspace verification.
3. **Workspace Verification (BETA):** The preset rule **Items with Coincident snap points** does not affect Workspace verification.
4. **Workspace (BETA):** The preset rule **Items with Coincident snap points** is not transferred from Model to Workspace or from Workspace to Model.

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
- **Clash Reporter Create View Points — BETA**
- **Stamper — ALPHA / Coming Soon**
- **Clash Reporter Images — ALPHA / Coming Soon**

## Future Plans

- Continue stabilization of Tests Editor custom clash-rule discovery and Workspace rule-state verification/transfer coverage.
- Continue validation of BETA workflows based on project use and tester feedback.
- Continue Stamper development before enabling it in a future Public Release.
- Continue development of Clash Reporter image export before enabling it in a future Public Release.
- Expand Analyzer, Workspace, reporting, and coordination workflows.

## Author

Developed by Mustafa Hesham.
