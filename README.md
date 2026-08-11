# Leviathan
LabVIEW codebase for the Leviathan STM-Break Junction.


## About

The Leviathan is a semi-automated scanning tunnelling microscope break junction instrument. This software is a hardware control and data acquisition system for Leviathan. 

### Features:

* A PID feedback controller to re-adjust the piezo between data acquisition chunks (ramps/traces) to compensate for thermal drift.

* High speed data acquisition. Currently hardware limited to 200 kHz sampling with efficient data logging in ASCII format. No binary saving required!

* Real-Time data acquisition and visualisations, e.g. single trace/1D conductance histograms/2D conductance-distance heatmaps.

* Multi-producer / multi-consumer architecture for efficient synchronised timing & minimal computational overhead.

* Advanced piezo & bias ramping modes with a modular design architecture for rapid addition of new experiments.  
  (e.g. standard STMBJ ramps, current-voltage, piezo holding, piezo-modulation/oscillation, bias-modulation/oscillation, 2-terminal CV sweeps etc...).

## How to Cite

If you use this 'Leviathan' software in your research, please cite this specific artifact as follows:

> J. M. F. Morris, R. T. Abram, C. E. Spano, R. Listo, A. Larbi, Z. Irlam, and A. Vezzoli (2026). Leviathan: STMBJ Control System (Version 4.1.0). Zenodo. https://doi.org

## License

Copyright (C) 2026 James M. F. Morris, R. Tom Abram, Chiara E. Spano, Roberto Listo, Adam Larbi, Zo&euml; Irlam, and Andrea Vezzoli.

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

## Version History

The complete development history and changes up to the current release can be found in the `versionLog.txt` file included in this repository.



