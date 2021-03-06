PowerModels.jl Change Log 
=================

### Staged
- Added missing function for AC-TNEP models
- Added checks that tap ratios are non-zero
- Made all power model forms abstract types, to support future extensions
- Made matpower parser more robust to cases with line flow values
- Fixed a bug that prevented parsing of bus_names when buses have non-contiguous ids
- Fixed bounds correction units when angmin and angmax are 0.0

### v0.3.0
- Updated to JuMP v0.15 syntax
- Replaced PowerModels set data types with "ref" dictionary
- Refactored Matpower data processing to simplify editing network data after parsing
- Unified network data and solution formats and made them valid JSON documents
- Replaced JSON test files with Matpower test files
- Added documentation on internal JSON data format to DATA.md
- Updated TNEP models to work with Matpower parsing extensions
- Strengthened convex formulations with Lifted Nonlinear Cuts (LNCs)
- Added ability to easily inspect the JuMP model produced by PowerModels
- Added constraint templates to provide an abstraction layer between the network data and network constraint definitions
- Moved system wide phase angle difference bounds to the "ref" dictionary
- Refactored model definitions to be based on complex numbers

### v0.2.3
- Multiple improvements to Matlab file parsing
  - Added support Matlab cell arrays
  - Added support for Matpower bus_names
  - Added ability for reading non-standard Matpower data elements
- Added JuMP version v0.14 upper bound 

### v0.2.2
- Added Transmission Network Expansion Planning (tnep) problem.

### v0.2.1
- Added support for julia v0.5.0 and OS X
- Added line flows option for solution output
- Added initial documentation and helper functions
- Replaced Gurobi with Pajarito for MISOCP tests

### v0.2.0
- Complete re-write to type-based implementation using dynamic dispatch
- Incorporated abstract problem specifications
- Added type-based formulation abstractions

### v0.1.0
- Initial function-based implementation
