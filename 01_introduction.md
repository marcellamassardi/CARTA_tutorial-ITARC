---
layout: default
title: What is CARTA and why should I use it?
nav_order: 1
---

# CARTA Viewer: A Modern Tool for Exploring Astronomical Images

The **CARTA Viewer** (Cube Analysis and Rendering Tool for Astronomy) is a powerful, web-based application for visualizing and analyzing astronomical data. Designed with performance and usability in mind, CARTA enables astronomers to interact seamlessly with large datasets from facilities such as **ALMA (Atacama Large Millimeter/submillimeter Array)** and many other observatories. It provides high-performance rendering and interactive tools tailored for radio astronomy and beyond.

---

## 🌌 What is CARTA?

CARTA is a next-generation image viewer that runs in your web browser while leveraging a backend server for data access and processing. This architecture allows users to work efficiently with large FITS images and multi-dimensional data cubes without needing to download them locally.

It is particularly well-suited for radio and millimeter/submillimeter astronomy, where datasets can be extremely large and complex.

CARTA is built to replace legacy desktop tools with a responsive, browser-accessible interface that can handle large FITS images and data cubes efficiently. It separates the frontend (user interface) from backend services, enabling scalable and remote workflows.


---

✨ 

## Key Features

- **⚡ High Performance with Large Data Cubes**  
  CARTA streams data dynamically, allowing smooth interaction even with massive datasets.

- **🧭 Responsive Navigation**  
  Instantly pan, zoom, and explore regions of interest without lag, making it easy to move through high-resolution images.

- **📊 Real-Time Spectral Analysis**  
  Extract and visualize spectra from data cubes interactively, ideal for multi-channel observations.

- **🎯 Region-Based Statistics**  
  Define regions and immediately compute statistics, helping with source identification and analysis.

- **🔗 Linked Views and Multi-Panel Layouts**  
  Compare multiple images or datasets side-by-side, useful for multi-configuration or multi-wavelength studies.

- **🌐 Remote Data Access**  
  Work directly on data stored on servers or clusters without transferring large files to your local machine.

- **🖥️ Platform Independence**  
  Run CARTA in any modern browser—no complex installation required for the frontend.

- **✨Real-time rendering with GPU acceleration** (when available) CARTA achieves real-time rendering by streaming only the required portions of image data from the backend to the browser and using GPU-accelerated techniques to dynamically update the display as the user pans, zooms, or analyzes the dataset.

---

## 🧱 Architecture Overview

CARTA uses a **client-server model**:

- **Frontend (Browser):**  
  Provides an intuitive graphical interface for visualization and interaction.

- **Backend (Server):**  
  Handles file I/O, data processing, and communication with the frontend.

This separation enables scalable workflows and efficient handling of large datasets typical of ALMA and other observatories.

![The client-server scheme for CARTA](../images/browser-server.png)



---

## 📂 Supported Data

CARTA supports a range of astronomical data formats, including:

- **FITS images and cubes**
- **CASA image formats** (via backend support)

This makes it suitable for data from:

- ALMA  
- VLA
- ATCA new BIGCAT correlator  
- MeerKAT  
- SKA precursors and pathfinders  
- Optical and infrared observatories  

---

## 📚 Official CARTA Documentation

For comprehensive guides, tutorials, and technical references, visit the official CARTA resources:

- 🌐 **CARTA Website**  
  https://cartavis.org  

- 📖 **Documentation Portal**  
  https://cartavis.org/docs/  

- 🚀 **Getting Started Guide**  
  https://cartavis.org/docs/user_guide/getting_started.html  

- 🧭 **User Guide**  
  https://cartavis.org/docs/user_guide/  

- ⚙️ **Backend Installation & Configuration**  
  https://cartavis.org/docs/backend/  

- 🧑‍💻 **GitHub Repository**  
  https://github.com/CARTAvis/carta  

These resources include:

- Step-by-step tutorials  
- Feature explanations and workflows  
- Backend setup and deployment instructions  
- Developer and API documentation  


[Next: before to start →](02_before_to_start.md)



✨ Key Features

    High-performance visualization of large astronomical datasets
    Interactive image exploration (zoom, pan, rotate)
    Multi-dimensional data cube support
    Region creation and analysis tools
    Spectral profile visualization
    Customizable layouts and linked views
    Real-time rendering with GPU acceleration (when available)

