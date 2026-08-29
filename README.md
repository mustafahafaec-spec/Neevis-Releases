# Neevis (Latest Version v1.9.0)

**Neevis** is a productivity add-in for Autodesk Navisworks Manage 2026 and 2027. It provides Workspace-based clash analysis, Search Set authoring, clash-management and review workflows, reporting, saved-viewpoint tools, model-finding utilities, geometry export, hotkeys, and coordination tools.

> **BETA tools/features:** Search Set Builder, Workspace, Clash Reporter Create View Points, and Right Click Options remain under wider testing.
>
> **Coming Soon:** Clash Reporter image export is designated **ALPHA** and is not executable in the v1.9.0 Public Release. Automated Stamping and Create Stamping Rule also remain ALPHA.

## Main Tools

### Tests and Sets

- **Matrix to Tests** creates clash tests from an Excel matrix.
- **Tests Editor** exports clash-test settings to Excel and applies controlled edits back to Navisworks.
- **Search Set Builder (BETA)** creates, edits, arranges, imports, exports, and synchronizes Navisworks Search Sets. It supports folders, condition editing, AND/OR/NOT logic, undo/redo, model-derived Property Set/Property/Value helpers, Selection Tree assignment, and Excel workflows.

### Workspace and Reviewing

- **Workspace (BETA)** provides the shared Neevis Workspace used by Workspace-aware tools. It supports Workspace creation/loading, verification, synchronization, screening, export, shared settings, and Workspace appearance behavior.
- **Analyzer** provides Workspace-based clash analysis with Items, Groups, Combo Groups, Main Groups, verification, recorded clash history, Clash Summary, Clashes Table, Clashes Timeline, Priority Items, Excel reporting, and model isolation.
- **Universal Clash Capture Settings** controls clash-isolation/capture appearance consistently across supported Neevis workflows. It includes four viewing modes—Only Clashing Items, Inclusive Clash Items, All Clashing Items, and All Elements—plus focal-element selection, Item A/Item B appearance, surrounding-clash appearance, non-clashing appearance, and status-based clash inclusion/color overrides.
- **Stamper** provides Manual Stamping for reviewing clashes one-by-one and classifying them during a focused controller workflow. **Automated Stamping** and **Create Stamping Rule** remain ALPHA and show **Coming Soon** in the Public Release.
- **Viewpoint Manager** organizes saved viewpoints, supports comments and Navisworks text markups, exports and updates Excel reports with images, and exchanges viewpoint XML files.

### Clash Coordination

- **Clashes Data Transfer** exports and imports clash metadata between Navisworks files.
- **Clash Grouper** groups clashes using user-defined grouping criteria.
- **Right Click Options (BETA)** adds Neevis actions to the Navisworks selection context menu for clash isolation, grouping, report access, and restoring the view. The feature remains under wider host-version testing.

### Exporting and Reporting

- **Results Count** exports clash-result counts as a table or as a Search Set matrix.
- **Clash Reporter** creates configurable HTML clash reports with selectable fields, statuses, comments, grouping, filters, and split-report options. **Create View Points remains BETA. Clash Reporter image export is ALPHA and is unavailable in the v1.9.0 Public Release.**
- **NaviSolid** exports selected Navisworks geometry to DWG and transfers geometry to an opened AutoCAD drawing.
- **IFC Export** exports selected Navisworks geometry to IFC4.

### Utility Tools

- **Get Revit ID** copies Revit Element IDs from selected Navisworks objects.
- **By Revit ID** locates model objects using Revit Element IDs.

### Neevis

- **Hotkeys** assigns two-key shortcuts to Neevis tools and supported native Navisworks commands.
- **About** provides version, appearance, licensing, update controls, Auto Update, update-notification preferences, Universal Clash Capture Settings, and bug/suggestion reporting.

## v1.9.0 Highlights

- Adds a dedicated **Workspace (BETA)** ribbon entry and expands the Workspace into a shared foundation for Workspace-aware Neevis tools.
- Adds **Universal Clash Capture Settings** so Analyzer, Stamper, Clash Reporter capture workflows, and supported context actions use one consistent clash-view definition.
- Adds four capture/isolation modes, including **Inclusive Clash Items**, plus configurable clash-status scope and optional status-specific color overrides.
- Updates Analyzer isolation to follow Universal Clash Capture Settings and restore the model view when the Analyzer closes after isolation.
- Improves **Update Relevant Tests** so Analyzer resolves and processes Workspace-referenced tests with less unnecessary catalog work.
- Adds the **Stamper Manual Stamping** review workflow with focused clash viewing and optional clash box sectioning.
- Adds **Right Click Options (BETA)** for selection-driven clash actions directly from the Navisworks context menu.
- Refines Clash Reporter capture/viewpoint behavior and report configuration. **Image export remains ALPHA / Coming Soon in the Public Release.**
- Expands shared dark-mode, settings, icon, and Workspace UI consistency across the add-in.

## Analyzer Workspace Overview

An Analyzer Workspace is the shared reporting definition used by Analyzer and Workspace-aware Neevis workflows. It contains:

- **Items** — reporting building blocks backed by one or more Search Sets.
- **Groups** — clash relationships between Items.
- **Combo Groups** — multiple Groups treated as one reporting Group while retaining their underlying Mini Groups.
- **Main Groups** — ordered reporting categories containing Groups.
- **Records** — timestamped clash readings used for history and comparison.
- **Workspace Settings** — shared screening, appearance, and Workspace behavior used across supporting tools.

Workspace verification distinguishes missing or changed Search Sets and Clash Tests so users can resolve structural issues before relying on reporting results.

## Compatibility

- Autodesk Navisworks Manage 2026
- Autodesk Navisworks Manage 2027
- Windows x64
- .NET Framework 4.8
- AutoCAD is required for NaviSolid DWG export and transfer to an opened AutoCAD drawing.

## Current Testing / Coming Soon

- **Search Set Builder (BETA)** — available and under continued validation.
- **Workspace (BETA)** — available and under continued validation.
- **Right Click Options (BETA)** — available and under wider Navisworks context-menu testing.
- **Clash Reporter Create View Points (BETA)** — available and under continued validation.
- **Clash Reporter Images (ALPHA)** — **Coming Soon**; not executable in the v1.9.0 Public Release.
- **Automated Stamping / Create Stamping Rule (ALPHA)** — **Coming Soon** in the Public Release.

## Future Plans

- Continue stabilization of BETA workflows based on project use and tester feedback.
- Continue development of Clash Reporter image export before enabling it in a future Public Release.
- Continue development of Automated Stamping and Stamping Rule creation.
- Expand Analyzer, Workspace, reporting, and coordination workflows.

## Author

Developed by Mustafa Hesham.
