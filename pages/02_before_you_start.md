---
layout: default
title: How to access CARTA?
nav_order: 1
---

# 🚀 How to access CARTA?

**CARTA is fundamentally a web application and utilizes a client-server architecture.** The main components are:

- a **backend server**: focuses on computations of image data for visualization on the client side. It typically run on a powerful server or cluster with high-speed storage where users’ data reside.
- a **frontend client**:  receives the data from the server side and utilizes web technologies to render the data for users. It also serves as the graphical user interface (GUI) for users to interact with the CARTA application.

Ad additional **controller** handles the lifetime of the backend process and user login authentication in case of Institutional deployment.

From a user point of view, the CARTA Viewer can be used in different deployment modes depending on the reciprocal position of backend and frontend: 
- **Local/Desktop mode** when both client and server are on the same machine/system 
- **Server-based mode**, when the server is located where the data reside and the client connecting to it through a browser.
This flexibility allows users to work efficiently with both small and extremely large astronomical datasets.

The supported operating systems for the server (for CARTA v5.1) are:
- **Ubuntu Linux**: 22.04 LTS (Jammy Jellyfish) and 24.04 LTS (Noble Numbat)
- **Red Hat** Enterprise Linux / AlmaLinux / Rocky Linux: 8, 9
- **macOS**: 14 (Sonoma), and 15 (Sequoia). Earlier version of macOS may work but they are not tested.
- even if not officially supported, it is possible to use CARTA through the **Windows Subsystem** for Linux 2 (WSL2), with Ubuntu being the recommended Linux distribution.

The client only needs
-  access to a CARTA backend server (local or remote)
-  a modern web browser (Chrome, Firefox, Edge are recommended)


---

# Which mode works better for me?

## 🖥️ Local / Desktop Mode

In **local mode**, CARTA runs entirely on a personal machine:
To operate in local mode the CARTA backend is available for Linux, macOS, and containerized environments

Installation resources and instructions are available here:

- Official releases and binaries:  
  https://cartavis.org/docs/backend/installation/
- GitHub repository:  
  https://github.com/CARTAvis/carta

Precompiled binaries and Docker images are commonly provided to simplify deployment.

### How it works

- The CARTA backend is launched locally.
- The browser connects to `localhost`.
- Data (images, regions, preferences,...) files are read directly from the local filesystem.

If CARTA is run locally on your own computer, the session data is saved to a local directory. 
Users can export regions to text files in CASA Region Text Format (.crtf) or DS9 (.reg) format.
Images can be edited and saved in png or FITS formats. Note that saving in FITS format is available only for local mode.

### Advantages
- Simple setup for small to medium datasets
- No network dependency
- Fast access to local files
- Ideal for development, testing, and classroom use

---

## 🌐 Server Mode

In server mode, CARTA is deployed on a remote machine (e.g., cluster, institute server, or cloud environment) and made accessible through an URL that can be opened from the client browser.

### How it works
- The backend runs on a remote server.
- Users connect via a web browser.
- Data remains on the server, avoiding large transfers.

When using the CARTA server version (e.g., via the ALMA Science Archive), a carta-controller uses a MongoDB database on the remote server to record user data, including interface preferences, layout configurations, and workspaces.
The backend (carta_backend) handles computations and stores data for visualization, ensuring that if you are connected to a shared server, your session data (regions/stats) remains available. Regions created for analysis are registered on the server and shared among spatially matched images.

### Advantages
- Handles very large datasets efficiently
- Centralized data storage
- Suitable for multi-user environments
- Ideal for HPC clusters and institutional deployments (may need a controller for accounting and resource-sharing)

---

## 🔭 Example: accessing CARTA on the Italian ARC cluster

(: .note)
With an account on the Italian ARC cluster, users can have access to a minimum of 10TB of space and computing blades for at least 6 months. 
CARTA is among the long list of software tools available on the ItARC cluster: this is similar to run in the above described **local mode** without installing it CARTA your machine (this is a nice solution for Windows users!!!).
See [the ItARC-cluster webpage](https://arc.ira.inaf.it/support-and-tools/arc-cluster/) for more information.


### To access CARTA on the ItARC cluster:

- Request an account to the Italian ARC node writing an email to help-desk@alma.inaf.it

- follow the instructions on [the ItARC-cluster webpage](https://arc.ira.inaf.it/support-and-tools/arc-cluster/) to install a VPN GUI and launch it on your machine

- follow the instruction on the same link to access the cluster

> ssh -X -P 22 <your_account>@scheduler.ira.inaf.it
> ssh -X <your_account>@almabl<blade_number>.ira.inaf.it

Blades available to users are numbers 07, 08 and 13. Up to date table of availability are on [the ItARC-cluster webpage](https://arc.ira.inaf.it/support-and-tools/arc-cluster/)

This will point you to the /homes/<your_account> folder on the IRA repository.
Change your operation directory

>cd /iranet/groups/arc/homesarc/<your_account> 

to your folder on the ARC cluster: this is the folder where you should put your image files (see details on [the ItARC-cluster webpage](https://arc.ira.inaf.it/support-and-tools/arc-cluster/)).

>irainit load carta
>
>carta
>
>[2026-05-02 10:03:52.979Z] [CARTA] [info] CARTA is accessible at http://192.168.49.26:3002/?token=af2e643f-c265-450f-8889-c11595890e2c

gives you the URL that you can open in your can copy and paste to your browser to access CARTA.
Notice that CARTA will initially search images in the IRA repository folder. We suggest to move and operates on the ARC cluster folder, as described above.

---

## 🔭 Example: using CARTA with the ALMA Science Archive

CARTA can be used in combination with data from the ALMA Science Archive, enabling direct exploration of observational products without manual data handling. This exploits the **server mode**. 

### To access CARTA on the ALMA Science Archive:

- Search and select a dataset in the ALMA Science Archive https://almascience.nrao.edu/aq/
- Identify in the image previews or in the download panel the images that are of your interest
- Access the CARTA interactive interface by clicking the FITS / images of interest 

This is extremely useful if you have storage problems as you do not need to download images.

{: .important}
Remember that images in the ALMA Science Archive are **NOT intended to be ready for science**, also if in most of the cases they are extremely good. For ALMA cycles 2,3, and 4 we strongly recommend to use ARI-L images if available. In any case verify that the images are of suitable quality for your purposes or reproduce them by following the instruction in the ALMA Science Archive manual. 

[← Previous: What is CARTA?](01_introduction.md) [Next: Meeting the interface →](03_interface.md)
