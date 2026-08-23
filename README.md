# Neevis (Latest Version v1.7.1)

**Neevis** is a productivity add-in for Autodesk Navisworks Manage 2026 and 2027. It provides clash-management, Search Set authoring, saved-viewpoint workflows, reporting, model-finding, geometry export, hotkeys, and coordination utilities.

> **Search Set Builder remains BETA in v1.7.1.** It is available for practical project use and testing, while its Search Set synchronization, Selection Tree assignment, and Excel workflows continue to receive validation in future v1.7.x updates.

## Main Tools

### Tests and Sets

- **Matrix to Tests** creates clash tests from an Excel matrix.
- **Tests Editor** exports clash-test settings to Excel and applies controlled edits back to Navisworks.
- **Search Set Builder (BETA)** creates, edits, arranges, imports, exports, and synchronizes Navisworks Search Sets. It supports folders, condition editing, AND/OR/NOT logic, undo/redo, model-derived Property Set/Property/Value helpers, and Excel workflows.
- **Selection Tree Assigning** provides a dedicated Search Set scope window. It can inspect one Search Set, compare the scope of multiple Search Sets, show mixed selections, and assign one Selection Tree scope to multiple Search Sets.
- Search Set Builder provides both **Apply** and **Confirm**: Apply commits changes while keeping the Builder open; Confirm commits and closes the Builder.

### Clashes

- **Clashes Data Transfer** exports and imports clash metadata between Navisworks files.
- **Clash Grouper** groups clashes using user-defined grouping criteria.

### Utility Tools

- **Get Revit ID** copies Revit Element IDs from selected Navisworks objects.
- **By Revit ID** locates model objects using Revit Element IDs.

### Reviewing

- **Viewpoint Manager** organizes saved viewpoints, supports comments and Navisworks text markups, exports and updates Excel reports with images, and exchanges viewpoint XML files.

### Exporting and Reporting

- **Results Count** exports clash-result counts as a table or as a Search Set matrix. In the matrix, Search Sets form both axes and each populated pair contains the corresponding clash-result count.
- **Clash Reporter** creates configurable clash reports with selectable fields, statuses, comments, grouping options, and images.
- **NaviSolid** exports selected Navisworks geometry to DWG and transfers geometry to an opened AutoCAD drawing.
- **IFC Export** exports selected Navisworks geometry to IFC4.

### Neevis

- **Hotkeys** assigns two-key shortcuts to Neevis tools and supported native Navisworks commands. Native-command tabs include Home, Viewpoint, Review, View, Output, Item Tools, and Sectioning Tools, with search for faster command discovery.
- **About** provides version, appearance, licensing, update controls, Auto Update, update-notification preferences, and bug/suggestion reporting.

## v1.7.1 Highlights

- Improves **Search Set Builder (BETA)** reliability when reading and editing existing Search Set conditions and Selection Tree scopes.
- Adds the dedicated **Selection Tree Assigning** workflow for inspecting and assigning scopes across multiple Search Sets.
- Adds **Apply** so Search Set changes can be committed without closing the Builder.
- Improves large-model UI responsiveness by initially showing bounded Property Set, Property, and Value dropdown previews, with `...` available to load the full list when needed.
- Improves condition Value display, including preservation of exact text casing where required by existing Search Sets.
- Improves Selection Tree reconstruction for partial model/file scopes and avoids unnecessary full-model expansion when opening or confirming the Builder.
- Corrects **Results Count Matrix** so Search Sets are the matrix axes and each Search Set pair is represented once, with the symmetric duplicate cell shown as `-`.
- Adds an About preference to enable or disable notifications when a new public Neevis release is available, independently from Auto Update.

## Compatibility

- Autodesk Navisworks Manage 2026
- Autodesk Navisworks Manage 2027
- Windows x64
- .NET Framework 4.8
- AutoCAD is required for NaviSolid DWG export and transfer to an opened AutoCAD drawing.

## Future Plans

### Edits and upgrades
- Continue testing and stabilization of **Search Set Builder (BETA)**.
- Expand Tests Editor and Clash Reporter workflows.
- Add additional clash-image and viewpoint reporting workflows.

### New Tools
- **Reevis** — Revit integration workflows.
- **Stamper** — automated approving and reviewing of clashes.
- **Inspector** — area-focused inspection workflows.
- **COBie Wizard** — COBie sheet export workflows.
- **Quantity Surveyor** — model quantity-counting workflows.

## Author

Developed by Mustafa Hesham.
