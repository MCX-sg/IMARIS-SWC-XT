# IMARIS SWC XT (Python)

This repository contains a Python XT script for [Imaris](https://imaris.oxinst.com/) to export neuron morphologies as `.swc` files.

The script is designed for:
- Converting Imaris filament objects to SWC format
- Preserving node coordinates, radii, and parent-child relationships
- avoid environment conflicts
- Making the output compatible with neuron simulators / analysis tools (e.g. Arbor, NEURON, etc.)

## Citation


Xu, Mengze; *IMARIS SWC XT: A Python script for exporting neuron morphologies from Imaris*, GitHub repository, 2025.  
https://github.com/MCX-sg/IMARIS-SWC-XT

> Note: This code was developed and tested with Imaris 10.2.0 on Windows.

---

## Features

- Export all filaments in the current Imaris scene to individual `.swc` files
- Create a folder under `documents` named `ImarisExports` 
- Basic handling of soma, dendrites, and axons (depending on how your filaments are annotated)
- Simple error messages when no suitable filament objects are found
- No use of external numpy and tkinker other than the embedded icepy in Imaris

---

## Installation

### 1. Requirements

- **Imaris** with XT (XTension) support
- **Python** (3.7)
- Python packages:
  - `ImarisLib`
  - `from __future__ import annotations`
  - `os`
  - `time`
  - `datetime`
### 2. File location
  - Put python script under XT folder within Imaris
  - Remember to link python to Imaris in custom tools
  - Close and reopen Imaris
  - You should see `Export Filament in SWC format` under Image Processing dropdown menu


## Known Limitations
  - Does not automatically return node type, therefore the second column on SWC file will return 0 even for the soma
