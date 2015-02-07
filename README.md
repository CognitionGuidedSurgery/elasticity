elasticity
==========

    Author: Nicolai Schoch
    Maintainer: Alexander Weigl <Alexander.Weigl@student.kit.edu
    Date: 2014-11-28
    License: elasticity is closed source
             Documentation under GPL v3

Soft tissue simulation based on Hiflow³

[cite paper please]


## Installation

Download the latest *elasticity* binary for your system:

* [Linux 64bit](https://raw.githubusercontent.com/CognitionGuidedSurgery/elasticity/master/bin/elasticity.lx64)
* Linux 32bit (not supported)
* Windows (not supported)

You should consider [hf3lint](https://github.com/areku/hf3lint)
for checking the input files for elasticity.

## Input Files

Two input files, one with the simulation setup (hf3), giving information such as input files, material properties, mathematical simulation framework, etc., and the other one with constraints (bcdata.xml), giving information such as pointwise displacement (Dirichlet) and force/pressure (Neumann) boundary conditions.
Each input file is in XML format. 

[Hf3 file specification](https://github.com/CognitionGuidedSurgery/elasticity/wiki/Hiflow%C2%B3-Elasticity-Input-File)
[BC file specification](https://github.com/CognitionGuidedSurgery/elasticity/wiki/BC-file)

