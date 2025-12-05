# IMARIS SWC XT (Python)

This repository contains a Python XT script for [Imaris](https://imaris.oxinst.com/) to export neuron morphologies as `.swc` files.

The script is designed for:
- Converting Imaris filament objects to SWC format
- Preserving node coordinates, radii, and parent-child relationships
- Making the output compatible with neuron simulators / analysis tools (e.g. Arbor, NEURON, etc.)

> Note: This code was developed and tested with Imaris 10.2.0 on Windows.

---

## Features

- Export all filaments in the current Imaris scene to individual `.swc` files
- Create a folder under 'documents' named 'ImarisExports'  
- Basic handling of soma, dendrites, and axons (depending on how your filaments are annotated)
- Simple error messages when no suitable filament objects are found

---

## Installation

### 1. Requirements

- **Imaris** with XT (XTension) support
- **Python** (the version Imaris is configured to use, e.g. 3.x)
- Python packages (if any):
  - `ImarisLib`
  - `from __future__``annotations`
  - `os`
  - `time`
  - `datetime`
  
