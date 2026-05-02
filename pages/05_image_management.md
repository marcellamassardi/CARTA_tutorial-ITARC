---
layout: default
title: Image management
nav_order: 1
---

# 🖼️ CARTA Image Management Guide

CARTA provides a flexible and efficient system for managing astronomical images and data cubes. Users can load, organize, compare, and export data through an intuitive interface designed for both simple and advanced workflows.

---

## 📂 Opening Images

Images can be loaded into CARTA from local or remote file systems.

### How to Open an Image
- Use the **File Browser** panel
- Navigate to your data directory
- Select a file (e.g., FITS image or cube)
- Click **Open**

### Result
- The image is displayed in the active viewer (frame)
- It appears in the **File List / Layer Panel**

---

## ➕ Appending Images

Appending allows you to load additional images without replacing the current one.

### How to Append
- Select another file in the File Browser
- Click **Append** instead of Open

### Result
- The new image is added to the session
- It can be displayed in the same or a different frame
- Useful for comparisons and overlays

---

## 🧩 Displaying Images in Different Frames

CARTA supports multiple viewer panels (frames).

### Creating a New Frame
- Add a new viewer panel from the layout controls  
- Or split the existing view

### Assigning Images to Frames
- Drag and drop an image from the **File List** into a frame  
- Or select the frame and choose the image to display  

### Benefits
- Side-by-side comparison  
- Multi-wavelength analysis  
- Viewing different channels of a cube  

---

## 🔗 Spatial Matching (Image Alignment)

When working with multiple images, CARTA can align them spatially.

### How to Enable Spatial Matching
- Activate **linked views** or **spatial matching** from the interface  
- Ensure images have valid WCS (World Coordinate System) information  

### What Happens
- Images align based on sky coordinates  
- Panning and zooming are synchronized  
- Cursor positions correspond across frames  

### Use Cases
- Comparing observations from different telescopes  
- Multi-frequency or multi-epoch studies  

---

## 📊 Overlay and Comparison

Images can be overlaid for enhanced analysis.

### Options
- Display one image as a raster and another as **contours**  
- Adjust transparency and color maps  
- Toggle visibility from the **Layer Panel**

---

## 💾 Exporting and Saving Images

CARTA allows exporting full images or selected regions.

---

### 🧾 Export as FITS

### How to Export
- Select the desired image or region  
- Use the export/save option in the interface  
- Choose **FITS format**

### Features
- Preserves scientific data and metadata  
- Can export:
  - Entire image  
  - Subregions  
  - Selected channels from cubes  

---

### 🖼️ Export as PNG

### How to Export
- Select the current view or region  
- Choose **PNG format**

### Features
- Saves a visual representation  
- Includes applied colormap and scaling  
- Ideal for presentations and publications  

---

### ✂️ Exporting Regions (Subimages)

- Define a region using region tools  
- Export only that portion of the image  
- Works for both FITS and PNG formats  

---

## ❌ Closing Images and Frames

### Closing an Image
- Remove it from the **File List / Layer Panel**  
- This unloads the data from the session  

### Closing a Frame
- Close or remove the viewer panel  
- Does not delete the image, only the view  

### Notes
- Multiple frames can display the same image  
- Closing a frame does not affect other frames  

---

## 🧠 Best Practices

- Use **append** to build multi-image workflows  
- Use **multiple frames** for comparison  
- Enable **spatial matching** for aligned analysis  
- Export **FITS** for scientific use, **PNG** for visualization  

---

## 📌 Summary

CARTA’s image management system allows users to:

- 📂 Open and append multiple datasets  
- 🧩 Organize images across multiple frames  
- 🔗 Align images spatially using WCS  
- 💾 Export data in scientific (FITS) or visual (PNG) formats  
- ❌ Efficiently close and manage resources  

This flexibility makes CARTA a powerful tool for handling complex astronomical datasets.



[← Previous: Setting Layouts and Preferences](04_layouts.md) [Next: How to define Regions →](06_regions.md)