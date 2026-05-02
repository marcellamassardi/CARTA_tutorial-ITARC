---
layout: default
title: Choose the way to access CARTA
nav_order: 1
---

### 🚀 Getting Started with CARTA 

CARTA is fundamentally a web application and utilizes a client-server architecture. There are three main components:

- a server: focuses on computations of image data for visualization on the client side. It typically run on a powerful server or cluster with high-speed storage where users’ data reside.
- a client:  receives the data from the server side and utilizes web technologies to render the data for users. It also serves as the graphical user interface (GUI) for users to interact with the CARTA application.
- a controller: handles the lifetime of the backend process and user login authentication (used only for Institutional deployment).

From a user point of view, the CARTA Viewer can be used in different deployment modes depending on the reciprocal position of backend and frontend: a **local/desktop mode** when both client and server are on the same machine a **server-based mode**, when the server located where the data reside and the client connecting to it through a browser. This flexibility allows users to work efficiently with both small and extremely large astronomical datasets.

The supported operating systems for the server (for CARTA v5.1) are:
- Ubuntu Linux: 22.04 LTS (Jammy Jellyfish) and 24.04 LTS (Noble Numbat)
- Red Hat Enterprise Linux / AlmaLinux / Rocky Linux: 8, 9
- macOS: 14 (Sonoma), and 15 (Sequoia). Earlier version of macOS may work but they are not tested.

While the client needs
-  a modern web browser (Chrome, Firefox, Edge are recommended)
-  access to a CARTA backend server (local or remote)

### Which mode works for me?

## 🖥️ Local / Desktop Mode

In **local mode**, CARTA runs entirely on a personal machine:
To operate in local mode the CARTA backend is available for Linux, macOS, and containerized environments

Installation resources are available here:

- Official releases and binaries:  
  https://cartavis.org/docs/backend/installation/
- GitHub repository:  
  https://github.com/CARTAvis/carta

Precompiled binaries and Docker images are commonly provided to simplify deployment.

# How it works
- The CARTA backend is launched locally.
- The browser connects to `localhost`.
- Data files are read directly from the local filesystem.

If CARTA is run locally on your own computer, the session data is saved to a local directory instead of a remote server. 
Users can export regions to text files in CASA Region Text Format (.crtf) or DS9 (.reg) format.
Images can be edited and saved in png or FITS formats.

# Advantages
- Simple setup for small to medium datasets
- No network dependency
- Fast access to local files
- Ideal for development, testing, and classroom use


## 🌐 Server Mode

In server mode, CARTA is deployed on a remote machine (e.g., cluster, institute server, or cloud environment) and made accessible trhough an URL that can be opened from the client browser.

### How it works
- The backend runs on a remote server.
- Users connect via a web browser.
- Data remains on the server, avoiding large transfers.

When using the CARTA server version (e.g., via the ALMA Archive), a carta-controller uses a MongoDB database on the remote server to record user data, including interface preferences, layout configurations, and workspaces.
The backend (carta_backend) handles computations and stores data for visualization, ensuring that if you are connected to a shared server, your session data (regions/stats) remains available. Regions created for analysis are registered on the server and shared among spatially matched images.

# Advantages
- Handles very large datasets efficiently
- Centralized data storage
- Suitable for multi-user environments
- Ideal for HPC clusters and institutional deployments (may need a controller for accounting and resource-sharing)

## 🔭 Example: accessing CARTA on the Italian ARC cluster
- Request an account to the Italian ARC node writing an email to help-desk@alma.inaf.it (this will give you a minimum of 10TB of space for 6 months with access to our computing blades. See https://arc.ira.inaf.it/support-and-tools/arc-cluster/ for more information.)


>cd /iranet/groups/arc/homesarc/<your_account> 

brings you to your folder on the ARC cluster: this is the folder where you should put your image files (see below).

{: .code}
>irainit load carta
>carta
[2026-05-02 10:03:52.979Z] [CARTA] [info] CARTA is accessible at http://192.168.49.26:3002/?token=af2e643f-c265-450f-8889-c11595890e2c

gives an URL that you can copy in your browser (t)



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

- 🖥️ Local mode → quick setup, local file access
- 🌐 Server mode → scalable, remote, multi-user analysis
- 🔭 ALMA Archive workflow → direct exploration of real observational data

This flexibility makes CARTA a powerful tool for both individual researchers and large scientific collaborations working with modern astronomical datasets.

[← Previous: Introduction](01_introduction.md) [Next: Meeting the interface →](03_interface.md)
