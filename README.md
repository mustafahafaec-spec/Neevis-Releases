# Neevis (Latest Version v1.9.1)

**Neevis** is a productivity add-in for Autodesk Navisworks Manage 2026 and 2027. It provides Workspace-based clash analysis, Search Set authoring, clash-management and review workflows, reporting, saved-viewpoint tools, model-finding utilities, geometry export, hotkeys, and coordination tools.

> **BETA tools/features:** Search Set Builder, Workspace, Clashes Data Transfer, Stamper, Clash Reporter Create View Points, and Right Click Options remain under wider testing.
>
> **Coming Soon:** Clash Reporter image export, Automated Stamping, and Create Stamping Rule remain **ALPHA** and are not executable in the v1.9.1 Public Release.

## Main Tools

### Tests and Sets

- **Matrix to Tests** creates clash tests from an Excel matrix.
- **Tests Editor** exports clash-test settings to Excel and applies controlled edits back to Navisworks.
- **Search Set Builder (BETA)** creates, edits, arranges, imports, exports, and synchronizes Navisworks Search Sets. It supports folders, condition editing, AND/OR/NOT logic, undo/redo, model-derived Property Set/Property/Value helpers, Selection Tree assignment, and Excel workflows.

### Workspace and Reviewing

- **Workspace (BETA)** provides the shared Neevis Workspace used by Workspace-aware tools. It supports Workspace creation/loading, verification, synchronization, screening, export, shared settings, Workspace appearance behavior, protected Analyzer Records, and staged Model/Workspace verification repair.
- **Analyzer** provides Workspace-based clash analysis with Items, Groups, Combo Groups, Main Groups, verification, recorded clash history, Clash Summary, Clashes Table, Clashes Timeline, Priority Items, reporting, and model isolation. Workspace/general settings are shared through the Workspace while Report settings remain user/machine preferences.
- **Universal Clash Capture Settings** controls clash-isolation/capture appearance consistently across supported Neevis workflows. It includes four viewing modes—Only Clashing Items, Inclusive Clash Items, All Clashing Items, and All Elements—plus focal-element selection, Item A/Item B appearance, surrounding-clash appearance, non-clashing appearance, and status-based clash inclusion/color overrides.
- **Stamper (BETA)** provides Manual Stamping for focused clash review and classification, including multi-clash highlighting and temporary review-view control. **Automated Stamping** and **Create Stamping Rule** remain ALPHA and show **Coming Soon** in the Public Release.
- **Viewpoint Manager** organizes saved viewpoints, supports comments and Navisworks text markups, exports and updates Excel reports with images, and exchanges viewpoint XML files.

### Clash Coordination

- **Clashes Data Transfer (BETA)** exchanges selected clash metadata between the model and Workspace and supports background **Automatic Sync** using configured Clash Tests, statuses, and data fields.
- **Clash Grouper** groups clashes using user-defined grouping criteria with optimized startup/property discovery for larger coordination models.
- **Right Click Options (BETA)** adds Neevis actions to the Navisworks selection context menu for clash isolation, grouping, report access, IFC export, and restoring the view. Clash actions use Workspace tests when a Workspace is loaded and all tests otherwise.

### Exporting and Reporting

- **Results Count** exports clash-result counts as a table or as a Search Set matrix.
- **Clash Reporter** creates configurable HTML clash reports with selectable fields, statuses, comments, grouping, filters, and split-report options. **Create View Points remains BETA. Clash Reporter image export is ALPHA and is unavailable in the v1.9.1 Public Release.**
- **NaviSolid** exports selected Navisworks geometry to DWG and transfers geometry to an opened AutoCAD drawing.
- **IFC Export** exports Navisworks geometry to IFC4. The main workflow lets the user choose export content from the Selection Tree, while the Right Click Options shortcut exports the current selection directly.

### Utility Tools

- **Get Revit ID** copies Revit Element IDs from selected Navisworks objects.
- **By Revit ID** locates model objects using Revit Element IDs.

### Neevis

- **Hotkeys** assigns two-key shortcuts to Neevis tools and supported native Navisworks commands.
- **About** provides version, appearance, licensing, update controls, Auto Update, update-notification preferences, Universal Clash Capture Settings, and bug/suggestion reporting.

## v1.9.1 Highlights

- Protects shared **Analyzer Records** with focused Workspace transactions so ordinary refresh/settings activity does not replace another user's newer records.
- Overhauls **Workspace Verification** with simplified Model/Workspace comparison, staged repair, pre-confirm unresolve, synchronized pane selection/scrolling, and broader Workspace-to-model restoration attempts.
- Adds **Clash Test - Conditions Changed** verification for tolerance/type differences.
- Separates Analyzer configuration so Workspace/general settings remain Workspace-owned while **Report settings are user/machine settings**.
- Combines Analyzer report actions under one **Report** control and makes Refresh reload current Workspace changes.
- Adds **Automatic Sync** to **Clashes Data Transfer (BETA)** with background bidirectional synchronization and most-recent-change conflict resolution.
- Improves **Stamper (BETA)** multi-clash review, view reset behavior, clash-result resolution, and selection/view responsiveness.
- Reduces **Clash Grouper** startup work by deferring heavy verification/property discovery until after first paint and reusing sampled model items.
- Refines **Right Click Options (BETA)** scope behavior and adds direct IFC Export access.
- Updates the main **IFC Export** workflow to choose content from the Selection Tree.
- Keeps **Clash Reporter Images** and **Automated Stamping / Create Stamping Rule** as ALPHA **Coming Soon** features in the Public Release.

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
- **Clashes Data Transfer (BETA)** — available with user/machine settings and Automatic Sync under continued validation.
- **Stamper (BETA)** — Manual Stamping is available and under continued validation.
- **Right Click Options (BETA)** — available and under wider Navisworks context-menu testing.
- **Clash Reporter Create View Points (BETA)** — available and under continued validation.
- **Clash Reporter Images (ALPHA)** — **Coming Soon**; not executable in the v1.9.1 Public Release.
- **Automated Stamping / Create Stamping Rule (ALPHA)** — **Coming Soon** in the Public Release.

## Future Plans

- Continue stabilization of BETA workflows based on project use and tester feedback, including Workspace, Clashes Data Transfer, Stamper, and Right Click Options.
- Continue development of Clash Reporter image export before enabling it in a future Public Release.
- Continue development of Automated Stamping and Stamping Rule creation.
- Expand Analyzer, Workspace, reporting, and coordination workflows.

## Author

Developed by Mustafa Hesham.
