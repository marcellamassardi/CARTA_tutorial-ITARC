---
layout: default
title: Guide on plotting Tools
nav_order: 1
---

# 📊 Plotting & Overlay Tools in CARTA

The **CARTA Viewer** provides a powerful set of plotting and overlay tools to enhance visualization and enable deeper analysis of astronomical data. These tools allow users to combine multiple data products, highlight structures, and integrate external information directly within the interface.

---

## 🧭 Overview

CARTA’s plotting capabilities are tightly integrated with the image viewer and support:

- Multi-layer visualization  
- Real-time updates  
- Interactive customization  
- Integration with external data sources  

---

## 🌀 Overlaying Contours

Contours are used to highlight intensity levels in an image.

### How to Use
1. Load an image (or multiple images)  
2. Select the image to use for contours  
3. Enable **Contour Overlay** from the layer or settings panel  
4. Adjust contour levels and styling  

### Customization Options
- Contour levels (manual or automatic)  
- Line color and thickness  
- Smoothing options  

### Use Cases
- Highlight faint emission structures  
- Compare different datasets (e.g., contours from one image over another)  

---

## ⭐ Overlaying Source Catalogues

CARTA can display catalogued astronomical sources directly on images.

### How to Use
1. Load or import a catalogue file (e.g., table with coordinates)  
2. Enable **Catalogue Overlay**  
3. Match coordinates with the image (via WCS)  

### Features
- Markers at source positions  
- Labels and metadata display  
- Filtering and selection options  

### Use Cases
- Identify known sources  
- Cross-match observations with catalogues  
- Visualize object distributions  

---

## 🧭 Overlaying Polarization Vectors

Polarization data can be visualized as vectors on the image.

### How to Use
1. Load polarization-related data (e.g., Stokes parameters)  
2. Enable **Vector Overlay**  
3. Configure vector display  

### Customization Options
- Vector length scaling  
- Orientation (angle)  
- Density of vectors  
- Color mapping  

### Use Cases
- Study magnetic field structures  
- Analyze polarization properties of sources  

---

## 🎞️ Channel Map Mode

Channel map mode displays multiple slices of a spectral cube simultaneously.

### How to Enable
- Activate **Channel Map Mode** from the display settings  

### Features
- Grid of images, each representing a different channel  
- Adjustable number of panels  
- Linked navigation across channels  

### Use Cases
- Visual inspection of spectral evolution  
- Identifying emission features across channels  
- Comparing structures at different velocities  

---

## 📐 Image Fitting

CARTA provides tools to fit models directly to image data.

### How to Use
1. Select a region of interest  
2. Open the **Image Fitting Tool**  
3. Choose a model (e.g., Gaussian)  
4. Run the fit  

### Output
- Model parameters (position, amplitude, size, etc.)  
- Residual maps (difference between data and model)  

### Use Cases
- Source characterization  
- Measuring sizes and fluxes  
- Identifying compact structures  

---

## 🌐 Online Queries

CARTA supports querying external astronomical databases.

### How to Use
1. Open the **Online Query** panel  
2. Specify search parameters (e.g., coordinates, radius)  
3. Select a service (catalogues, surveys)  
4. Retrieve and overlay results  

### Features
- Direct integration with online archives  
- Automatic coordinate matching  
- Overlay results on the image  

### Use Cases
- Cross-identification of sources  
- Accessing complementary datasets  
- Enriching analysis with external information  

---

## 🔗 Combining Multiple Overlays

CARTA allows multiple overlays simultaneously:

- Contours + catalogues  
- Vectors + channel maps  
- External data + local images  

All overlays are:
- Dynamically updated  
- Individually customizable  
- Toggleable for clarity  

---

## ⚡ Performance Considerations

- Overlays are rendered efficiently using GPU acceleration  
- Only visible data is processed and displayed  
- Large catalogues can be filtered to maintain performance  

---

## 💡 Best Practices

- Use contours to emphasize structure without obscuring the base image  
- Adjust catalogue density to avoid clutter  
- Scale polarization vectors appropriately for readability  
- Use channel maps for quick inspection, then switch to single-view for detailed analysis  
- Combine overlays carefully to maintain visual clarity  

---

## 📌 Summary

CARTA’s plotting tools enable rich, multi-layered visualization:

- 🌀 Contours → highlight intensity structures  
- ⭐ Catalogues → display known sources  
- 🧭 Polarization vectors → visualize directional data  
- 🎞️ Channel maps → explore spectral cubes  
- 📐 Image fitting → model sources  
- 🌐 Online queries → integrate external data  

These tools make CARTA a comprehensive environment for both visualization and scientific analysis of astronomical datasets.


[← Previous: How to define Regions](06_regions.md) [Next: What you need for Spectral analysis →](08_spectral_analysis.md)