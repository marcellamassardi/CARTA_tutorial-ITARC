---
layout: default
title: What is CARTA and why should I use it?
nav_order: 1
---

# The CARTA viewer

# CARTA Viewer

The **CARTA Viewer** (Cube Analysis and Rendering Tool for Astronomy) is a modern, web-based application designed for the visualization and analysis of large astronomical image data. It provides high-performance rendering and interactive tools tailored for radio astronomy and beyond.

## 🚀 Overview

CARTA is built to replace legacy desktop tools with a responsive, browser-accessible interface that can handle large FITS images and data cubes efficiently. It separates the frontend (user interface) from backend services, enabling scalable and remote workflows.

## ✨ Key Features

- **High-performance visualization** of large astronomical datasets
- **Interactive image exploration** (zoom, pan, rotate)
- **Multi-dimensional data cube support**
- **Region creation and analysis tools**
- **Spectral profile visualization**
- **Customizable layouts and linked views**
- **Real-time rendering with GPU acceleration (when available)**

## 🧱 Architecture

CARTA uses a client-server architecture:

- **Frontend**: Runs in the browser and provides the user interface
- **Backend**: Handles data access, processing, and streaming

This design allows users to work with large datasets stored remotely without needing to download them locally.

## 📂 Supported Data Formats

- FITS (Flexible Image Transport System)
- CASA image formats (via backend support)

## 🛠️ Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Edge recommended)
- Access to a CARTA backend server (local or remote)

### Running CARTA

1. Start the CARTA backend server:
   ```bash
   carta_backend


**bold face**
*italic* 

![text to show](../images/05.01_science_plan_overview.png)

{: .tip}
>content of blocks

---

## SUbsession

[Aladin interactive sky atlas](https://aladin.cds.unistra.fr/aladin.gml) 
![Individual pointings](../images/05.06_field_setup_target_type.png)

{: .tip}
> 1. In the visualiser, select "Show pointing positions" to overlay the pointings mosaic to the selected rectangle. 
> 2. When you change a value in the "Rectangle" section, press "tab" to update the visualizer. 

{: .note }
> No interactivity is currently implemented for rectangles in the visualiser — you cannot drag or resize the rectangle. All parameters must be entered manually. The "Show pointing positions" toggle displays the individual pointings within the rectangle.

{: .tip }
> Pointings can be defined in **CARTA** and imported into the OT using the import button. This is especially useful for complex mosaic patterns. The file format must match what the OT expects — consult the [OT documentation](https://almascience.eso.org/proposing/observing-tool) for the specification.

{: .important }
> something important

[link to other file](06_science_background.md) 



---

[← The Proposal section](04_proposal_section.md) · [Next: Science background →](06_science_background.md)
