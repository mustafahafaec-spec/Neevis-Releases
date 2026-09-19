# Neevis (Latest Version v1.9.9)

**Neevis** is a productivity add-in for Autodesk Navisworks Manage 2026 and 2027. It provides Workspace-based clash analysis, Search Set authoring, clash-management and review workflows, reporting, saved-viewpoint tools, model-finding utilities, geometry export, hotkeys, and coordination tools.

> **BETA tools/features:** Search Set Builder, Clashes Data Transfer, and Right Click Options remain under wider testing.

> **Coming Soon:** Stamper, Reporter Create View Points, and Reporter image export are **ALPHA** and are not executable in the v1.9.9 Public Release.

## Main Tools

### Tests and Sets

- **Matrix to Tests** creates clash tests from an Excel matrix.
- **Tests Editor** exports clash-test settings to Excel and applies controlled edits back to Navisworks. Large Excel imports and applies use cached baselines, batched host updates, and optimized built-in Clash Detective rule handling.
- **Search Set Builder (BETA)** creates, edits, arranges, imports, exports, and synchronizes Navisworks Search Sets. It supports folders, condition editing, AND/OR/NOT logic, undo/redo, model-derived Property Set/Property/Value helpers, Selection Tree assignment, and Excel workflows.

### Workspace and Analyzer

- **Workspace** provides the shared Neevis Workspace used by Workspace-aware tools. The central Workspace is a single portable **`.nws`** file with independently compressed and revisioned data sections.
- Workspace stores coordination definitions, shared settings, Analyzer records, cache-file update information, per-test clash records, clash metadata/group membership, source-file relationships, synchronized Viewpoints, and supporting cross-host identity.
- Workspace includes direct **Reset and Update Tests**, **Delete Non-Workspace Tests**, and **Clear Workspace Data** actions. Screened Workspace tests are protected from the non-Workspace deletion action.
- **Workspace Verification** compares model and Workspace definitions and provides detailed selected-error differences for Search Set conditions, Clash Test definitions, assignments, and related Workspace data.
- Workspace-aware Clash Test updating uses trusted run/cache signatures so unchanged tests are not rerun merely because Navisworks reports them as `Old`. When a real update is required, Neevis prepares the relevant Search Set content once and runs the required tests as a batch.
- **Analyzer** provides Workspace-based clash analysis with Items, Groups, Combo Groups, Main Groups, recorded clash history, Clash Summary, Clashes Table, **Clashes Matrix**, Priority Items, Clashes Timeline, reporting, and model isolation.
- Analyzer automatic report updating occurs when a clash recording is successfully created; normal window refreshes and settings changes do not automatically rewrite the report.
- Analyzer **General settings are local per user/machine**. Workspace-specific definitions and records remain Workspace data.
- Analyzer isolation follows the statuses selected under **Statuses included in Total**; clashes moved to excluded statuses are removed from the active isolated clash view.
- **Universal Clash Capture Settings** controls clash-isolation/capture appearance consistently across supported Neevis workflows.
- **Viewpoint Manager** organizes saved viewpoints, supports comments and Navisworks text markups, exports and updates Excel reports with images, and imports/exports Navisworks Viewpoints XML. Duplicate viewpoint names are supported without collapsing their identities.

### Centralization and Clash Coordination

- **Sync Data** is the explicit central synchronization workflow. It performs authoritative Workspace verification, then synchronizes the selected data. **Sync All** processes the full unscreened Workspace scope; **Sync Specific** lets the user choose unscreened Main Groups and remembers that selection for later sessions.
- Sync Data updates only Workspace Clash Tests that actually require rerunning and scopes Sync Specific test updating, Clashes Data, and Clash Groups to the selected Main Groups.
- **Clashes Data Transfer (BETA)** exchanges selected clash metadata between the model and Workspace. Reviewed and Approved are the synchronized review-status scope; metadata fields include Priority, Description, Comments, Assigned To, and Approved By. Central reconciliation remains field-aware and change-driven.
- **Clash Groups** is synchronized with Clashes Data through the same progress stage while group membership remains a separate data concept from review metadata.
- **Sync Data – Viewpoints** synchronizes Workspace Saved Viewpoints, folders, and supported saved visibility/appearance attributes between verified models. Native Navisworks Viewpoints XML is the authoritative camera/tree transport, while Neevis safely reapplies saved attributes, protects against stale deletion states and duplicate GUID collisions, and preserves complete camera/frustum state when attribute-bearing viewpoints are recaptured.
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
- **Reporter** creates configurable HTML clash reports with selectable fields, statuses, comments, grouping, filters, and split-report options. Reporter initialization defers expensive Workspace/filter hydration so the window can appear sooner. **Create View Points is ALPHA / Coming Soon** and is unavailable in the Public Release.
- **Reporter image export is ALPHA / Coming Soon** and is unavailable in the Public Release.
- **NaviSolid** exports selected Navisworks geometry to DWG and transfers geometry to an opened AutoCAD drawing.
- **IFC Export** exports Navisworks geometry to IFC4. The main workflow lets the user choose export content from the Selection Tree, while the Right Click Options shortcut exports the current selection directly.
- **Reeviz Portal** connects Neevis/Navisworks to Reeviz in Revit. It receives the active Revit section box, shows a loading window while geometry is processed, excludes the originating Revit model from return sources, and returns intersecting Navisworks geometry/source information for Revit transfer.

### Settings and Updates

- **About** provides version, appearance, licensing, update controls, Auto Update, update-notification preferences, Universal Clash Capture Settings, and bug/suggestion reporting.
- Neevis settings can be exported and loaded from About for supported tools, allowing user preferences to be transferred between installations.

### Coming Soon

- **Stamper (ALPHA)** remains visible as an under-development tool but does not execute in the v1.9.9 Public Release.
- **Reporter Images (ALPHA)** remains visible as Coming Soon and does not execute in the Public Release.

## Compatibility

- Autodesk Navisworks Manage 2026
- Autodesk Navisworks Manage 2027
- Windows x64
- .NET Framework 4.8
- AutoCAD is required for NaviSolid DWG export and transfer to an opened AutoCAD drawing.

## Current Testing / Coming Soon

- **Search Set Builder — BETA**
- **Clashes Data Transfer — BETA**
- **Right Click Options — BETA**
- **Reporter Create View Points — ALPHA / Coming Soon**
- **Stamper — ALPHA / Coming Soon**
- **Reporter Images — ALPHA / Coming Soon**

## Future Plans

- Continue optimizing very large Clashes Data synchronization without reducing transfer correctness.
- Continue validation of remaining BETA workflows based on project use and tester feedback.
- Continue Stamper development before enabling it in a future Public Release.
- Continue development of Reporter Create View Points and image export before enabling them in a future Public Release.
- Expand Workspace-based interoperability with Reeviz and other coordination workflows.

## Author

Developed by Mustafa Hesham.
