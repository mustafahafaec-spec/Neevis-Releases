# Neevis (Latest Version v1.9.2)

**Neevis** is a productivity add-in for Autodesk Navisworks Manage 2026 and 2027. It provides Workspace-based clash analysis, Search Set authoring, clash-management and review workflows, reporting, saved-viewpoint tools, model-finding utilities, geometry export, hotkeys, and coordination tools.

> **BETA tools/features:** Search Set Builder, Workspace, Clashes Data Transfer, Right Click Options, and Clash Reporter Create View Points remain under wider testing.
>
> **Coming Soon:** Stamper and Clash Reporter image export are **ALPHA** and are not executable in the v1.9.2 Public Release.

## Main Tools

### Tests and Sets

- **Matrix to Tests** creates clash tests from an Excel matrix.
- **Tests Editor** exports clash-test settings to Excel and applies controlled edits back to Navisworks.
- **Search Set Builder (BETA)** creates, edits, arranges, imports, exports, and synchronizes Navisworks Search Sets. It supports folders, condition editing, AND/OR/NOT logic, undo/redo, model-derived Property Set/Property/Value helpers, Selection Tree assignment, and Excel workflows. v1.9.2 strengthens Confirm/move/rename safety and prevents Neevis hotkeys from firing while Search Set names or folders are being edited.

### Workspace and Analyzer

- **Workspace (BETA)** provides the shared Neevis Workspace used by Workspace-aware tools. It supports Workspace creation/loading, verification, synchronization, screening, export, shared settings, Workspace appearance behavior, Analyzer Records, cache-file awareness, and staged Model/Workspace verification repair.
- **Analyzer** provides Workspace-based clash analysis with Items, Groups, Combo Groups, Main Groups, recorded clash history, Clash Summary, Clashes Table, **Clashes Matrix**, Clashes Timeline, Priority Items, reporting, and model isolation.
- Analyzer **General settings are local per user/machine**. Workspace-specific definitions and records remain Workspace data.
- Analyzer isolation follows the statuses selected under **Statuses included in Total**; clashes moved to excluded statuses are removed from the active isolated clash view.
- **Universal Clash Capture Settings** controls clash-isolation/capture appearance consistently across supported Neevis workflows.
- **Viewpoint Manager** organizes saved viewpoints, supports comments and Navisworks text markups, exports and updates Excel reports with images, and exchanges viewpoint XML files.

### Clash Coordination

- **Clashes Data Transfer (BETA)** exchanges selected clash metadata between the model and Workspace and supports manual/automatic synchronization using configured Clash Tests, statuses, groups, and data fields.
- **Clash Grouper** groups clashes using user-defined grouping criteria with optimized startup/property discovery for larger coordination models.
- **Right Click Options (BETA)** adds Neevis actions to the Navisworks selection context menu. v1.9.2 adds **Review Related Clashes** and **Approve Related Clashes** for clashes that exist exclusively between selected elements, alongside isolation, grouping, report access, IFC export, and view reset actions.

### Exporting and Reporting

- **Results Count** exports clash-result counts as a table or as a Search Set matrix.
- **Clash Reporter** creates configurable HTML clash reports with selectable fields, statuses, comments, grouping, filters, and split-report options. **Create View Points remains BETA** and its loading process can be cancelled safely.
- **Clash Reporter image export is ALPHA / Coming Soon** and is unavailable in the Public Release.
- **NaviSolid** exports selected Navisworks geometry to DWG and transfers geometry to an opened AutoCAD drawing.
- **IFC Export** exports Navisworks geometry to IFC4. The main workflow lets the user choose export content from the Selection Tree, while the Right Click Options shortcut exports the current selection directly.

### Utility Tools

- **Get Revit ID** copies Revit Element IDs from selected Navisworks objects.
- **By Revit ID** locates model objects using Revit Element IDs.
- **Hotkeys** assigns two-key shortcuts to Neevis tools and supported native Navisworks commands. Hotkeys are suppressed while text/label editing is active so renaming Search Set folders cannot trigger commands.
- **About** provides version, appearance, licensing, update controls, Auto Update, update-notification preferences, Universal Clash Capture Settings, and bug/suggestion reporting.

### Coming Soon

- **Stamper (ALPHA)** remains visible as an under-development tool but does not execute in the v1.9.2 Public Release.
- **Clash Reporter Images (ALPHA)** remains visible as Coming Soon and does not execute in the Public Release.

## v1.9.2 Highlights

- Adds the Analyzer **Clashes Matrix** with Workspace Item/Search Set axes, optional Search Set detail, heat map, multi-cell selection, context actions, Excel report output, persisted Matrix display settings, and a live **Highlighted Clashes = n** count.
- Adds Analyzer **Reset Model Appearances** and **Apply WS Appearances** controls beside **Update Workspace Tests** across report tabs.
- Makes Analyzer General settings local and makes active isolation follow the configured included clash statuses.
- Adds **Review Related Clashes** and **Approve Related Clashes** to Right Click Options for selected-to-selected clashes.
- Adds cancellation to Clash Reporter **Create View Points** processing.
- Strengthens Search Set Builder Confirm, folder move/rename behavior, hierarchy mutation safety, and hotkey suppression during text editing.
- Expands Workspace cache-file/path verification and staged repair workflows while retaining Workspace as a BETA feature.
- Refines Clashes Data Transfer Sync/Export settings and Workspace-aware synchronization behavior.

## Known Issue

- **Workspace Verification (BETA):** verification/apply of Search Sets assigned to nested subfiles inside federated/repathed model files remains under development. In affected workflows, verify nested Search Set assignments manually after source/path changes before relying on Workspace repair.

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

- Continue stabilization of Workspace Verification, including nested Search Set sub-assignment repair.
- Continue validation of BETA workflows based on project use and tester feedback.
- Continue Stamper development before enabling it in a future Public Release.
- Continue development of Clash Reporter image export before enabling it in a future Public Release.
- Expand Analyzer, Workspace, reporting, and coordination workflows.

## Author

Developed by Mustafa Hesham.
