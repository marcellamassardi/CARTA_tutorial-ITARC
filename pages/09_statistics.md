---
layout: default
title: Statistics widget
nav_order: 1
---
PAGE UNDER CONSTRUCTION


# 📊 Statistics Widget in CARTA

The **Statistics Widget** in the CARTA Viewer provides real-time quantitative analysis of image data within a selected region or the entire image. It is a fundamental tool for extracting physical and statistical properties from astronomical datasets.

---

## 🧭 Overview

The Statistics Widget computes numerical summaries of pixel values:

- Within a **selected region** (recommended)
- Or across the **full image**

Results update dynamically as:
- Regions are moved or resized  
- Channels change in spectral cubes  
- Different images are selected  

---

## ▶️ How to Use

1. Load an image or spectral cube  
2. Define a **region** (or use the full image)  
3. Open the **Statistics Widget**  
4. Select:
   - The image layer  
   - The region of interest  

The widget will immediately display computed values.

---

## 📐 Available Statistical Quantities

Below are the main quantities provided by CARTA, along with their definitions.

---

### 🔢 Number of Pixels (N)

Total number of pixels in the selected region.

\[
N = \text{number of valid pixels}
\]

---

### 📏 Sum

Total sum of pixel values:

\[
\text{Sum} = \sum_{i=1}^{N} x_i
\]

**Use:** Total flux (for intensity-calibrated images)

---

### 📉 Mean (Average)

Average pixel value:

\[
\mu = \frac{1}{N} \sum_{i=1}^{N} x_i
\]

**Use:** Average brightness in a region

---

### 📊 Median

Middle value when pixel values are sorted.

**Use:** Robust estimate of central value (less sensitive to outliers)

---

### 📈 Minimum and Maximum

\[
\text{Min} = \min(x_i), \quad \text{Max} = \max(x_i)
\]

**Use:** Identify extrema (e.g., peak emission)

---

### 📉 Standard Deviation (RMS)

Measure of dispersion:

\[
\sigma = \sqrt{ \frac{1}{N} \sum_{i=1}^{N} (x_i - \mu)^2 }
\]

**Use:**
- Noise estimation  
- Signal-to-noise calculations  

---

### 📊 Variance

\[
\sigma^2 = \frac{1}{N} \sum_{i=1}^{N} (x_i - \mu)^2
\]

**Use:** Spread of data values

---

### 📏 Sum of Squares

\[
\sum x_i^2
\]

**Use:** Intermediate quantity for advanced analysis

---

### 📐 Flux Density (Context-Dependent)

If the image is calibrated, the **sum** may represent integrated flux (e.g., Jy).

**Note:** Interpretation depends on:
- Units of the image  
- Beam size (for radio data)  

---

## 🎚️ Spectral Cube Support

For spectral cubes, statistics can be computed:

- Per **channel** (slice)  
- Across **selected channel ranges**  
- Dynamically while navigating channels  

---

## 🔗 Region-Based Analysis

Statistics are tightly linked to regions:

- Multiple regions can be analyzed simultaneously  
- Each region produces independent statistics  
- Results update in real time  

---

## ⚙️ Additional Features

- Exclude invalid or masked pixels  
- Support for NaN handling  
- High-performance computation for large datasets  

---

## 💡 Best Practices

- Use **regions** instead of full images for meaningful results  
- Estimate noise using emission-free regions (RMS)  
- Use **median** for robustness against outliers  
- Track statistics across channels for spectral analysis  

---

## 📌 Summary

The CARTA Statistics Widget enables users to:

- 📊 Compute real-time statistics on image data  
- 📍 Analyze specific regions of interest  
- 🎚️ Explore variations across spectral cubes  
- 📐 Extract scientifically meaningful quantities  

It is an essential tool for transforming visual data into quantitative insight in astronomical analysis.




[← Previous: What you need for Spectral analysis ](08_spectral_analysis.md) [Next: Tips and Tricks →](10_tips.md)
