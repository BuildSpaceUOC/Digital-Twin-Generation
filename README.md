# 🏗️ IFC Model Generation Tools

This repository contains three Python-based tools for generating [IFC] files from different input formats. These tools are designed to support digital twin generation through geometry extraction and BIM data modeling.

---

## Modules Overview

### 1. `geometric_extraction.ipynb`

- Extracts geometric features (e.g. surfaces, lines) from point cloud or mesh data.
- Supports segmentation, normal estimation, and visualization.
- Intended for preprocessing before IFC model creation.

---

### 2. `obj2ifc.py`

- Converts `.obj` mesh files into `.ifc` models using a template (blueprint) IFC file.
- Creates an `IfcRoof` element based on mesh geometry.
- Includes placement, representation, and spatial containment.

**Input:**
- `input_obj_file.obj` — the source OBJ file.
- `sample.ifc` — the IFC template/blueprint.

**Output:**
- `output_roof.ifc`

---

### 3. `txt2ifc.py`

- Converts facade and opening coordinates from `.txt` files into full IFC models.
- Creates `IfcWallStandardCase`, `IfcOpeningElement`, and `IfcWindow`.
- Assigns materials, quantities, and basic property sets.

**Input:**
- `facade01.txt` — defines wall geometry.
- `rectangle_txt/cluster_*.txt` — defines openings/windows.

**Output:**
- `wall_window_test.ifc`

---
