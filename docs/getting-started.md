# Getting Started

This guide will help you get up and running with aeroflux.

## Installation

*Note: aeroflux is currently in development. Packaging and 'pip install' support are planned for Phase 2.*

To use aeroflux now, clone the repository and install dependencies:

```bash
git clone https://github.com/moebessd/aeroflux.git
cd aeroflux
pip install -r requirements.txt
```

## Quick Start

The following example demonstrates how to build a UCRM wing geometry and generate a 3D visualization:

```python
from pathlib import Path
from aeroflux.geometry.ucrm import build_ucrm_geometry

# Build UCRM geometry with 4 sections
wing = build_ucrm_geometry(4)

# Generate a 3D plot and save as HTML
wing.plot_wing_3d(
    show_panels=True,
    show_sections=False,
    show_grid=False,
    pov="top",
    save_dir=Path("wing_geometry.html"),
)
```
