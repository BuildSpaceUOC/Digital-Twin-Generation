# Geometric Feature Extraction from Point Clouds

This repository contains a comprehensive Jupyter Notebook for extracting **geometric structures**—such as windows and walls—from point cloud data using **Open3D**, **DBSCAN**, and **RANSAC** techniques.

The pipeline includes:

-**Clustering** of window and wall instances with `DBSCAN`
-**RANSAC** for plane segmentation
-**Normal filtering** to extract vertical planes
-**Batch processing** of planes into separate wall clusters
-**Renaming and mapping** of instances
-Extraction of **plane coefficients** (`A, B, C, D`)
-**Boundary rectangle fitting** on 2D projections

---

## Features

| Step | Description |
|------|-------------|
| `DBSCAN` | Clusters point cloud into individual wall/window segments |
| `RANSAC` | Detects large planes like building facades |
| `Vertical Filtering` | Filters only vertical planes using surface normals |
| `Batch Plane Clustering` | Runs DBSCAN over all detected planes |
| `File Renaming` | Renames wall files sequentially and saves mappings |
| `Plane Coefficient Extraction` | Saves each plane's `(A, B, C, D)` equation |
| `Boundary Rectangle Fitting` | Fits a bounding rectangle in the projected 2D space |

---

## Output Directory Structure

```bash
instance_wall_vertical_02/
  ├── plane_00_01.ply
  ├── ...

renamed_walls_vertical_02/
  ├── plane_000.ply
  ├── ...
  ├── mapping_table.txt
  ├── wall_plane_coefficients.txt

boundary_rectangles_vertical_02/
  ├── plane_000_boundary_rectangle.ply
