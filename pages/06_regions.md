---
layout: default
title: How to define Regions
nav_order: 1
---

```md id="carta-regions"
# 📍 Regions in CARTA: Definition, Import, and Export

Regions are a core feature of the **CARTA Viewer**, allowing users to define areas of interest on astronomical images for visualization, measurement, and analysis. CARTA provides a variety of region types and flexible tools to create, edit, import, and export them.

---

## ✏️ Defining Regions

Regions can be created interactively using the **toolbar**.

### How to Create a Region
1. Select a region tool from the toolbar  
2. Click and drag on the image viewer  
3. Adjust the shape using control handles  

### Interactive Features
- Resize, rotate, and move regions  
- Snap to coordinates (if enabled)  
- Modify properties (color, label, line style)  

Regions are immediately active and linked to analysis tools such as statistics and spectral profiles.

---

## 🔷 Types of Regions

CARTA supports several geometric region shapes:

### ⭕ Circle
- Defined by center and radius  
- Useful for compact sources  

---

### ◻️ Rectangle
- Defined by width and height  
- Can be rotated  
- Ideal for structured regions or cutouts  

---

### 🔶 Ellipse
- Defined by major/minor axes and orientation  
- Suitable for extended sources  

---

### 🔺 Polygon
- Defined by multiple vertices  
- Highly flexible for irregular shapes  

---

### 📏 Line / Polyline
- Defined by two or more points  
- Used for profile extraction or slices  

---

### 🎯 Point
- Single coordinate location  
- Useful for marking positions  

---

## 🧾 Region Properties

Each region includes metadata and customizable properties:

- Name / label  
- Color and style  
- Coordinate system (pixel or world coordinates)  
- Locked/unlocked state  

---

## 📥 Importing Regions

CARTA allows importing region definitions created externally.

### Supported Formats
- Common astronomy region formats (e.g., DS9 region files)

### How to Import
- Use the **Region Panel** or menu  
- Select a region file from your system  

### Result
- Regions are overlaid on the image  
- Automatically aligned using WCS (if available)  

---

## 📤 Exporting Regions

Regions can be saved for reuse or sharing.

### How to Export
- Select one or more regions  
- Use the export/save option  

### Output
- Region definition files (e.g., DS9 format)  
- Preserves geometry, position, and properties  

---

## 🔗 Regions and Analysis

Regions are tightly integrated with CARTA’s analysis tools.

### Capabilities
- Compute statistics (mean, RMS, sum, etc.)  
- Extract spectral profiles from cubes  
- Compare multiple regions simultaneously  

### Dynamic Updates
- Results update in real time when regions are moved or resized  

---

## 🧩 Managing Multiple Regions

CARTA supports working with many regions at once.

### Features
- List of all regions in the **Region Panel**  
- Toggle visibility  
- Group and organize regions  
- Delete or duplicate regions  

---

## 💡 Best Practices

- Use **simple shapes** (circle, rectangle) for quick analysis  
- Use **polygons** for complex structures  
- Import regions to **reuse previous work**  
- Export regions to **share results or ensure reproducibility**  

---

## 📌 Summary

CARTA’s region system allows users to:

- ✏️ Define regions interactively  
- 🔷 Use a variety of geometric shapes  
- 📥 Import regions from external tools  
- 📤 Export regions for reuse and sharing  
- 📊 Perform real-time analysis within selected areas  

Regions are essential for extracting meaningful scientific information from astronomical images and data cubes.
```


[← Previous: Image Management](05_image_management.md) [Next: Guide on plotting Tools →](07_tools.md)
