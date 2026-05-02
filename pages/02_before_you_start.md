---
layout: default
title: PAGE UNDER CONSTRUCTION
nav_order: 1
---

## 🚀 Getting Started with CARTA

The CARTA Viewer can be used in different deployment modes depending on the user’s needs: a **local/desktop mode**, a **server-based mode**, or through direct integration with external data archives such as the **ALMA Science Archive**. This flexibility allows users to work efficiently with both small and extremely large astronomical datasets.

## Prerequisites

-  A modern web browser (Chrome, Firefox, Edge recommended)
-  Access to a CARTA backend server (local or remote)


## Persistence
- **Persistent State**: When using the CARTA server version (e.g., via the ALMA Archive), a carta-controller uses a MongoDB database on the remote server to record user data, including interface preferences, layout configurations, and workspaces.
- **Regions**: Regions created for analysis are registered on the server and shared among spatially matched images.
- **Session Information**: The backend (carta_backend) handles computations and stores data for visualization, ensuring that if you are connected to a shared server, your session data (regions/stats) remains available.

## Data Independence & Local Usage
- **Independence**: When an image is unmatched from the spatial reference, it receives an independent copy of the regions, which can then be managed separately.
- **Local/Desktop Mode**: If CARTA is run locally on your own computer, this session data is saved to a local directory instead of a remote server.
- **Exporting Data**: Users can export regions to text files in CASA Region Text Format (.crtf) or DS9 (.reg) format.

## Key Takeaways for Privacy
- **Multi-user Servers**: In a shared environment, your regions and session stats are stored on that server's backend.
- **ALMA/Archive Usage**: If utilizing CARTA via remote archives (e.g., ALMA/ESO), your session and created regions are part of that remote session, not local, unless explicitly exported

---

## 💾 Downloading CARTA

CARTA does not require a traditional installation in the browser, but the backend application must be installed or accessed depending on the chosen workflow.

### 🔧 Backend Download

The CARTA backend is available for Linux, macOS, and containerized environments:

- Official releases and binaries:  
  https://cartavis.org/docs/backend/installation/

- GitHub repository:  
  https://github.com/CARTAvis/carta

Precompiled binaries and Docker images are commonly provided to simplify deployment.

---

## 🖥️ Local / Desktop Mode

In **local mode**, CARTA runs entirely on a personal machine:
## How it works
- The CARTA backend is launched locally.
- The browser connects to `localhost`.
- Data files are read directly from the local filesystem.

### Typical workflow
> bash carta_backend
Then open [http://localhost:3000](http://localhost:3000) in your web browser.

### Advantages
- Simple setup for small to medium datasets
- No network dependency
- Fast access to local files
- Ideal for development, testing, and classroom use


## 🌐 Server Mode

In server mode, CARTA is deployed on a remote machine (e.g., cluster, institute server, or cloud environment):

### How it works
- The backend runs on a remote server.
- Users connect via a web browser.
- Data remains on the server, avoiding large transfers.

### Typical workflow
- Start backend on remote system

Access via URL such as: https://your-server-address:port

### Advantages
- Handles very large datasets efficiently
- Centralized data storage
Suitable for multi-user environments
- Ideal for HPC clusters and institutional deployments


## 🔭 Example: using CARTA with the ALMA Science Archive

CARTA can be used in combination with data from the ALMA Science Archive, enabling direct exploration of observational products without manual data handling.

### Workflow
Search and select a dataset in the ALMA Science Archive
https://almascience.nrao.edu/asax/
Download or access the FITS / image products associated with observations

### Benefits for ALMA data analysis
- Direct visualization of calibrated ALMA images and spectral cubes
- Efficient exploration of large interferometric datasets
- Interactive spectral and spatial analysis without preprocessing overhead
- Seamless integration with standard FITS products


##📌 Summary

CARTA supports multiple workflows:

🖥️ Local mode → quick setup, local file access
🌐 Server mode → scalable, remote, multi-user analysis
🔭 ALMA Archive workflow → direct exploration of real observational data

This flexibility makes CARTA a powerful tool for both individual researchers and large scientific collaborations working with modern astronomical datasets.

