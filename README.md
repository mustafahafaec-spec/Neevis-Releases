# Neevis (Latest Version v1.8.0)

**Neevis** is a productivity add-in for Autodesk Navisworks Manage 2026 and 2027. It provides clash analysis and reporting, Search Set authoring, clash-management workflows, saved-viewpoint tools, model-finding utilities, geometry export, hotkeys, and coordination tools.

> **Search Set Builder remains BETA in v1.8.0.** It is available for practical project use and testing while its Search Set synchronization, Selection Tree assignment, and Excel workflows continue to receive validation.

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

- **Analyzer** provides a Workspace-based clash-analysis workflow. Workspaces organize Search Sets into Items, Groups, Combo Groups, and Main Groups, verify their source Search Sets and Clash Tests, store timestamped clash records, and drive live reports from the current Navisworks model. Analyzer includes Clash Summary, Clashes Table, Clashes Timeline, and Priority Items reports, plus clash isolation, optional post-isolation coloring, Item-based model coloring, and Excel report export.
- **Viewpoint Manager** organizes saved viewpoints, supports comments and Navisworks text markups, exports and updates Excel reports with images, and exchanges viewpoint XML files.

### Exporting and Reporting

- **Results Count** exports clash-result counts as a table or as a Search Set matrix. In the matrix, Search Sets form both axes and each populated pair contains the corresponding clash-result count.
- **Clash Reporter** creates configurable clash reports with selectable fields, statuses, comments, grouping options, and images.
- **NaviSolid** exports selected Navisworks geometry to DWG and transfers geometry to an opened AutoCAD drawing.
- **IFC Export** exports selected Navisworks geometry to IFC4.

### Neevis

- **Hotkeys** assigns two-key shortcuts to Neevis tools and supported native Navisworks commands. Native-command tabs include Home, Viewpoint, Review, View, Output, Item Tools, and Sectioning Tools, with search for faster command discovery.
- **About** provides version, appearance, licensing, update controls, Auto Update, update-notification preferences, and bug/suggestion reporting.

## v1.8.0 Highlights

- Adds **Analyzer**, a new clash-analysis and historical reporting workflow built around reusable Workspaces.
- Adds the **Workspace Wizard** for defining Items from Search Sets, Priority Items, Groups, Combo Groups, Main Groups, and report structure.
- Adds Workspace verification with Search Sets as the primary integrity check and Clash Test verification as a secondary check.
- Adds timestamped clash **Records** stored with the Workspace for historical comparison.
- Adds live **Clash Summary**, **Clashes Table**, **Clashes Timeline**, and **Priority Items** reporting views.
- Adds configurable clash-status inclusion, Main Group screening, report descriptions, and report-specific settings.
- Adds selected-Group clash isolation, Saved Viewpoint creation, and optional coloring of clashing Item A/Item B elements after isolation.
- Adds Item-based model coloring and a command to update the Workspace's relevant Clash Tests.
- Adds selectable **Excel report export** with formatted tables, historical data, and report charts.
- Improves **Search Set Builder (BETA)** so Selection Tree assignments can be edited independently for multiple Search Sets without repeatedly applying and reopening the workflow.
- Adds export/import of Search Set assignment mappings so matching Search Sets can receive the same assignments in another model.

## Analyzer Workspace Overview

An Analyzer Workspace is the reporting definition used by Analyzer. It contains:

- **Items** — reporting building blocks backed by one or more Search Sets. Items can be colored and marked as Priority Items.
- **Groups** — clash relationships between Items. A Group resolves the relevant Clash Tests from the Search Sets assigned to its Items.
- **Combo Groups** — multiple Groups treated as one reporting Group while their underlying Mini Groups remain available for editing.
- **Main Groups** — ordered reporting categories containing Groups.
- **Records** — timestamped clash readings used for history and comparison.
- **Settings** — report columns, clash statuses, screening, Priority Item options, and isolation-color behavior.

Workspaces can be created, loaded, edited, verified, moved to another location, and reused. Analyzer checks Workspace Search Sets and Clash Tests against the active model so changed or missing definitions can be reviewed before reporting.

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
