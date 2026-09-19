# Neevis v1.10.0

**Neevis** is a productivity and coordination add-in for **Autodesk Navisworks Manage 2026 and 2027**.

It is designed to make day-to-day BIM coordination faster by helping you create and maintain clash tests, manage Search Sets, review and report clashes, synchronize coordination data between models, manage viewpoints and model files, and exchange coordination geometry with Reeviz in Revit.

You can use many Neevis tools independently. For project-wide coordination, **Workspace** acts as the shared coordination layer and **Sync Data** keeps supported information aligned between verified Navisworks models.

---

## Start Here

If you are new to Neevis, the typical project workflow is:
1. **Tests and Sets** — prepare Search Sets and Clash Tests.
2. **Workspace** — create or load the project Workspace (`.nws`).
3. **Analyzer / Reporter** — review, analyze, record, and report clashes.
4. **Viewpoint Manager / Export tools** — organize viewpoints or export coordination data as needed.

If you only need a single utility, such as finding an element by Revit ID or exporting IFC, you can use that tool directly.

---

# Tools

## Tests and Sets

### Matrix to Tests
Creates Navisworks Clash Tests from an Excel clash matrix.

**Use it when:** you already have a coordination matrix in Excel and want to build the required Clash Tests automatically instead of creating them one by one.

### Tests Editor
Exports Clash Test definitions to Excel, lets you edit supported settings in a table, then applies the changes back to Navisworks.

**Use it when:** you need to review or update many Clash Tests faster than editing every test manually in Clash Detective.

### Search Set Builder — BETA
Creates and maintains Navisworks Search Sets from a dedicated editor and Excel workflow.

You can create folders and Search Sets, edit conditions, use AND / OR / NOT logic, assign model properties and values, import/export through Excel, and update existing Search Sets.

**Use it when:** you need to build or maintain a large, structured Search Set library.

---

## Utility Tools

### Get Revit ID
Copies the Revit Element ID from the selected Navisworks object to the clipboard.

**Use it when:** you need to identify the corresponding element in Revit.

### By Revit ID
Finds and selects a Navisworks object using its Revit Element ID.

**Use it when:** someone gives you a Revit Element ID and you need to locate that element in the federated Navisworks model.

---

## Clashes

### Clashes Data Transfer

Transfers supported clash review information between the current model and the Workspace.

Supported coordination data includes review status and fields such as Priority, Description, Comments, Assigned To, Approved By, and Clash Group information where applicable.

**Use it when:** multiple Navisworks models or users need to share clash-review information through the same Workspace.

### Clash Grouper
Groups clash results using defined criteria such as location, model information, properties, priority, or status.

**Use it when:** you need to turn a long flat clash list into practical coordination groups.

---

## Reviewing

### Analyzer
The main Workspace-based clash review and analysis tool.

Analyzer provides:

- Clash Summary
- Clashes Table
- Clashes Matrix
- Priority Items
- Clash Timeline
- Main Groups and Combo Groups
- Clash recordings/history
- Model isolation and review views
- Report and selected-test export workflows

Analyzer follows the active Workspace scope, including **Group Screen** and **Volume Screen** where applicable.

**Use it when:** you want to understand clash status, priorities, trends, relationships between disciplines, or review a focused part of the coordination model.

### Viewpoint Manager
Organizes Saved Viewpoints and supports comments, text markups, Excel reporting with images, and viewpoint import/export workflows.

It also supports **Operation Viewpoints** for transferring only the viewpoints currently included in an operation while preserving unrelated viewpoints.

**Use it when:** Saved Viewpoints are part of your coordination, review, or reporting workflow.

### Stamper — ALPHA / Coming Soon
An under-development clash review and stamping workflow.

The tool remains visible for development tracking but is **not available for normal use in the v1.10.0 Public Release**.

### Reporter
Creates configurable clash reports from Navisworks clash data.

You can control report fields, statuses, comments, grouping, filters, and report splitting.

**Use it when:** you need a shareable clash report for coordination meetings, issue distribution, or project records.

> **Coming Soon:** Reporter **Create View Points** and Reporter image export remain ALPHA and are not available for normal use in the v1.10.0 Public Release.

---

## Exporting

### Results Count
Exports clash-result counts as either a table or a Search Set-style matrix.

**Use it when:** you need a quick numerical clash summary for Excel, dashboards, or coordination tracking.

### NaviSolid
Exports selected Navisworks geometry to DWG and can transfer it to an opened AutoCAD drawing.

**Use it when:** you need solid/model geometry from Navisworks in AutoCAD.

> AutoCAD is required for the DWG transfer workflow.

### IFC Export
Exports Navisworks geometry to **IFC4**.

The main tool lets you choose export content from the Selection Tree. Neevis Right Click Options can also export the current selection directly.

**Use it when:** you need to create an IFC from selected/federated Navisworks geometry.

### Reeviz Portal
Connects Neevis in Navisworks with **Reeviz in Revit**.

Reeviz can send the active Revit Section Box to Neevis. Neevis identifies the intersecting Navisworks geometry and returns it for temporary transfer into Revit while excluding the originating Revit model.

The Portal supports source visibility controls, source colors, original Navisworks colors, and Section Box application for coordination checks.

**Use it when:** a Revit user needs surrounding federated Navisworks coordination geometry directly inside the current Revit view.

---

## Centralization

### Workspace
Workspace is the shared project coordination layer used by Workspace-aware Neevis tools.

A Workspace is stored as a portable **`.nws`** file and can hold project coordination definitions and shared data such as:

- Workspace Items and Groups
- Clash Test definitions and assignments
- Clash records and metadata
- Analyzer recordings
- Source-file relationships
- Saved Viewpoint synchronization data
- Shared coordination settings

Workspace also provides verification tools that compare the current Navisworks model with the loaded Workspace and identify differences that need attention.

### Group Screen
Group Screen limits Workspace-aware workflows to selected Workspace groups/items.

**Use it when:** you want to work only with a defined coordination group rather than the whole Workspace.

### Volume Screen — BETA
Volume Screen limits Workspace-aware workflows to a saved 3D **Volume Box**.

You can create, save, rename, recapture, and delete Volume Boxes or switch back to **Whole Model**.

Volume Screen is used by supported workflows including Analyzer, Reporter, Clash Grouper, Clashes Data Transfer, Stamper, and Sync Data.

**Use it when:** you want Neevis to focus on a specific building zone, floor, area, or 3D volume.

### Sync Data
Synchronizes supported information between the current verified Navisworks model and the loaded Workspace.

It supports full synchronization and selected Main Group synchronization, depending on the workflow and data type.

Supported synchronized data includes coordination information such as Clash Data, Clash Groups, and Saved Viewpoints where enabled.

**Use it when:** project models need to exchange the latest Workspace coordination data.

---

## File Tools

### Purger
Deletes selected categories of saved Navisworks model data.

**Use it when:** you need to clean unwanted saved information from the current Navisworks file.

### File Manager
Lists loaded model/cache files with their source information, paths, and update dates.

It supports reviewing, sorting, and managing loaded files, including removal/repath-related workflows.

**Use it when:** you need to inspect or manage the files that make up the federated Navisworks model.

---

## Neevis

### Hotkeys
Assigns two-key shortcuts to Neevis tools and supported Navisworks commands.

**Use it when:** you want faster keyboard access to frequently used coordination commands.

### About
Shows Neevis version and product information and provides access to supported settings, updates, appearance options, settings import/export, and feedback tools.

---

# Additional Neevis Features

## Right Click Options
Adds Neevis actions to the Navisworks selection context menu.

Depending on the selected objects and workflow, actions can include clash isolation, review/approval operations, grouping/report access, IFC export, and view reset commands.

## Universal Clash Capture Settings
Provides common clash-view/capture appearance settings used by supported Neevis clash workflows.

**Use it when:** you want clash isolation and capture views to follow a consistent visual standard.

---

# Feature Status

| Feature | Status |
| --- | --- |
| Search Set Builder | BETA |
| Volume Screen | BETA |
| Stamper | ALPHA / Coming Soon |
| Reporter Images | ALPHA / Coming Soon |

**BETA** features are available for use but are still under wider project validation.

**ALPHA / Coming Soon** features are still under development and are not enabled for normal use in the Public Release.

---

# Compatibility

- Autodesk Navisworks Manage 2026
- Autodesk Navisworks Manage 2027
- Windows x64
- .NET Framework 4.8
- AutoCAD required only for NaviSolid DWG transfer to an opened AutoCAD drawing

---

# Author

Developed by **Mustafa Hesham**.
