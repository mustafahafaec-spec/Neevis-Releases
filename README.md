# Neevis (Latest Version v1.7.0)

**Neevis** is a productivity add-in for Autodesk Navisworks Manage 2026 and 2027. It brings clash-management, Search Set authoring, saved-viewpoint workflows, reporting, model-finding, geometry export and more.

> **Search Set Builder is released as BETA in v1.7.0.** It is available for real project testing, but its Excel import/export and Navisworks Search Set synchronization workflows will continue to receive validation and fixes in future v1.7.x patches before the BETA designation is removed.

## Main Tools

### Tests and Sets

- **Matrix to Tests** creates clash tests from an Excel matrix.
- **Tests Editor** exports clash-test settings to Excel and applies controlled edits back to Navisworks.
- **Search Set Builder (BETA)** provides a workspace for creating, editing, arranging, importing, exporting, and synchronizing Navisworks Search Sets. It supports folders, drag/reorder operations, condition editing, AND/OR/NOT visualization, Selection Tree scope, undo/redo, Excel workflows, and model-derived Property Set/Property/Value helpers. Changes remain in the Builder workspace until the user confirms them.

### Clashes

- **Clashes Data Transfer** exports and imports clash metadata between Navisworks files.
- **Clash Grouper** groups clashes using user-defined grouping criteria.

### Utility Tools

- **Get Revit ID** copies Revit Element IDs from selected Navisworks objects.
- **By Revit ID** locates model objects using Revit Element IDs.

### Reviewing

- **Viewpoint Manager** organizes saved viewpoints, supports comments and Navisworks text markups, exports and updates Excel reports with images, and exchanges viewpoint XML files.

### Exporting and Reporting

- **Results Count** exports clash-result counts as a matrix or a table.
- **Clash Reporter** creates configurable clash reports with selectable fields, statuses, comments, grouping options, and images.
- **NaviSolid** exports selected Navisworks geometry to DWG and transfers geometry to an opened AutoCAD drawing.
- **IFC Export** exports selected Navisworks geometry to IFC4.

### Neevis

- **Hotkeys** assigns two-key shortcuts to Neevis tools and supported native Navisworks commands. Native-command tabs include Home, Viewpoint, Review, View, Output, Item Tools, and Sectioning Tools, with search for faster command discovery.
- **About** provides version, appearance, licensing, update controls, Auto Update, and bug/suggestion reporting.

## v1.7.0 Highlights

- Introduces **Search Set Builder (BETA)** to the public release line.
- Adds a substantially expanded Hotkeys manager with supported native Navisworks ribbon commands.
- Adds Auto Update controls and improved staged update handling.
- Adds bug/suggestion reporting from About.
- Refreshes Neevis and tool artwork, including dark-mode-aware main branding.
- Includes extensive Search Set Builder work on hierarchy reflection, Excel import/export, property identity handling, Selection Tree scopes, workspace undo/redo, drag ordering, and safety checks before modifying Navisworks.

## Compatibility

- Autodesk Navisworks Manage 2026
- Autodesk Navisworks Manage 2027
- Windows x64
- .NET Framework 4.8
- AutoCAD is required for NaviSolid DWG export and transfer to an opened AutoCAD drawing.

## Future Plans

### Edits and upgrades
- **Search Set Builder BETA** Continue testing and stabilization.
- **Clash Reporter**Add editing rules to Tests Editor
- **Clash Reporter** Make the report export clashes images
- **Clash Reporter** Convert clashes to view points
### New Tools
- **Reevis** A tool for Revit integration workflows.
- **Stamper** A tool for automated approving and reviewing clashes
- **Inspector** A tool for an area focused inspection
- **COBie Wizard** A tool for exporting COBie sheets from the Navisworks
- **Quantity Surveyor** A tool for quantity counting of the elements in the model 

## Author

Developed by Mustafa Hesham.
