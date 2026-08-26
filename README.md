# Neevis (Latest Version v1.8.1)

**Neevis** is a productivity add-in for Autodesk Navisworks Manage 2026 and 2027. It provides clash analysis and reporting, Search Set authoring, clash-management workflows, saved-viewpoint tools, model-finding utilities, geometry export, hotkeys, and coordination tools.

> **Search Set Builder remains BETA in v1.8.1.** It is available for practical project use and testing while its Search Set synchronization, Selection Tree assignment, and Excel workflows continue to receive validation.

## Main Tools

### Tests and Sets

- **Matrix to Tests** creates clash tests from an Excel matrix.
- **Tests Editor** exports clash-test settings to Excel and applies controlled edits back to Navisworks.
- **Search Set Builder (BETA)** creates, edits, arranges, imports, exports, and synchronizes Navisworks Search Sets. It supports folders, condition editing, AND/OR/NOT logic, undo/redo, model-derived Property Set/Property/Value helpers, and Excel workflows.
- **Selection Tree Assigning** provides a dedicated Search Set scope window. Different Search Sets can be assigned independently in the same session, and assignment mappings can be exported and imported between models by Search Set name.
- Search Set Builder provides both **Apply** and **Confirm**: Apply commits changes while keeping the Builder open; Confirm commits and closes the Builder.

### Clashes

- **Clashes Data Transfer** exports and imports clash metadata between Navisworks files.
- **Clash Grouper** groups clashes using user-defined grouping criteria.

### Utility Tools

- **Get Revit ID** copies Revit Element IDs from selected Navisworks objects.
- **By Revit ID** locates model objects using Revit Element IDs.

### Reviewing

- **Analyzer** provides a Workspace-based clash-analysis workflow. Workspaces organize Search Sets into Items, Groups, Combo Groups, and Main Groups; verify Search Sets and Clash Tests with Critical, Medium, and Minor issue levels; store timestamped clash records; and drive live reports from the current Navisworks model. Analyzer includes Clash Summary, Clashes Table, Clashes Timeline, and Priority Items reports, plus clash isolation, optional Saved Viewpoint creation, optional post-isolation coloring, Item-based model coloring, and Excel report export.
- **Viewpoint Manager** organizes saved viewpoints, supports comments and Navisworks text markups, exports and updates Excel reports with images, and exchanges viewpoint XML files.

### Exporting and Reporting

- **Results Count** exports clash-result counts as a table or as a Search Set matrix. In the matrix, Search Sets form both axes and each populated pair contains the corresponding clash-result count.
- **Clash Reporter** creates configurable clash reports with selectable fields, statuses, comments, grouping options, and images.
- **NaviSolid** exports selected Navisworks geometry to DWG and transfers geometry to an opened AutoCAD drawing.
- **IFC Export** exports selected Navisworks geometry to IFC4.

### Neevis

- **Hotkeys** assigns two-key shortcuts to Neevis tools and supported native Navisworks commands. Native-command tabs include Home, Viewpoint, Review, View, Output, Item Tools, and Sectioning Tools, with search for faster command discovery.
- **About** provides version, appearance, licensing, update controls, Auto Update, update-notification preferences, and bug/suggestion reporting.

## v1.8.1 Highlights

- Refines **Analyzer Workspace Verification** into three clear levels: Critical for missing Search Sets, Medium for missing Clash Tests, and Minor for changed Search Set definitions.
- Keeps Search Set verification and Clash Test verification separate while providing appropriate bulk-resolution actions for Medium and Minor issues.
- Standardizes **Combo Groups** so Item A shows the most repeated Item and Item B shows **Multiple**.
- Adds **Add View Point when isolate** to Analyzer Settings so Saved Viewpoint creation during isolation can be enabled or disabled per Workspace.
- Optimizes **Update Workspace Tests** so only required Workspace-referenced tests are processed, already-current tests are skipped, and the user's Navisworks Auto-Save preference is preserved around the update operation.
- Makes the first **Clash Summary** column manually resizable during the Analyzer session.
- Improves **Clashes Table** history by showing the newest Record first and displaying local time below each Record date.
- Renames the Clashes Table **Total** column to **Current Total** and widens it for clearer reading.
- Improves Clashes Table Excel export with centered cells, clearer Main Group boundaries, and no data bar for a zero Current Total value.

## Analyzer Workspace Overview

An Analyzer Workspace is the reporting definition used by Analyzer. It contains:

- **Items** — reporting building blocks backed by one or more Search Sets. Items can be colored and marked as Priority Items.
- **Groups** — clash relationships between Items. A Group resolves the relevant Clash Tests from the Search Sets assigned to its Items.
- **Combo Groups** — multiple Groups treated as one reporting Group while their underlying Mini Groups remain available for editing. Item A represents the most repeated Item in the Combo Group and Item B is shown as **Multiple**.
- **Main Groups** — ordered reporting categories containing Groups.
- **Records** — timestamped clash readings used for history and comparison.
- **Settings** — report columns, clash statuses, screening, Priority Item options, isolation-color behavior, and optional Saved Viewpoint creation during isolation.

Workspaces can be created, loaded, edited, verified, moved to another location, and reused. Analyzer checks Workspace Search Sets and Clash Tests against the active model before reporting. Verification distinguishes:

- **Critical** — a required Search Set cannot be found and must be resolved manually.
- **Medium** — a required Clash Test cannot be found and can be resolved automatically or manually.
- **Minor** — a Search Set definition changed and can be accepted automatically or reviewed manually.

Existing v1.8.0 Workspaces remain supported. If an older Workspace contains a Search Set change that cannot be safely classified from its legacy signature, Analyzer may require one-time manual confirmation before establishing the newer detailed verification baseline.

## Compatibility

- Autodesk Navisworks Manage 2026
- Autodesk Navisworks Manage 2027
- Windows x64
- .NET Framework 4.8
- AutoCAD is required for NaviSolid DWG export and transfer to an opened AutoCAD drawing.

## Future Plans

### Edits and upgrades
- Continue testing and stabilization of **Search Set Builder (BETA)**.
- Expand Analyzer reporting and coordination workflows.
- Expand Tests Editor and Clash Reporter workflows.

### New Tools
- **Reevis** — Revit integration workflows.
- **Stamper** — approving and reviewing clash results.
- **Inspector** — area-focused inspection workflows.
- **COBie Wizard** — COBie sheet export workflows.
- **Quantity Surveyor** — model quantity-counting workflows.

## Author

Developed by Mustafa Hesham.
