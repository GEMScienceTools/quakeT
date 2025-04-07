Auxiliary module
################################

The :index:`auxiliary` module contains codes that support the development of auxiliary functionalities 
required for simulating each fundamental phase of the earthquake process. 
It provides tools for statistical operations, spatial representations, and input/output (I/O) management. 
Additionally, it includes built-in databases such as ground motion models, correlation models, and other resources 
essential for the simulation workflow.

Pre-simulation
*********************************************

The pre-simulation submodule focuses on preparing and managing fault geometries before the main simulation steps. 
Its core functionalities include:

- **Fault information management**: 
  Import and modify fault segment data stored in GeoJSON format, including geometrical and attribute handling.

- **Geometry validation**: 
  Check and validate the geometric consistency of fault segments to ensure accurate meshing and simulation.

- **Triangular meshing**:
  Generate triangular meshes based on the fault geometry, enabling detailed structural representation.

- **STL file creation**:
  Convert the meshed fault segments into STL (Stereolithography or Standard Triangle Language) file format, 
  suitable for 3D visualization and numerical simulations.


Post simulation
*********************************************
  The post-simulation analysis focuses on processing the earthquake catalog, extracting statistical insights, 
  and creating visualizations to better understand the seismic event distribution.

- **Catalog processing**: 
  The earthquake catalog is loaded from a MATLAB `.mat` file. The catalog is then saved as a `.csv` file to facilitate easier access and further processing.

- **Statistical evaluation**: 
  Key earthquake parameters which are magnitude, rupture area, mean slip, and mean stress drop, are statistically summarized.

- **3D spatial visualization**: 
  3D scatter plots are created to visualize the spatial distribution of events.

- **Magnitude-frequency distribution (MFD)**: 
  MFDs of the simulated earthquake catalog are analyzed.
  Gutenberg-Richter law parameters, specifically the **a-value** and **b-value**, are estimated using various statistical techniques.
  Then, MFD plots are generated, illustrating the relationship between earthquake magnitude and the cumulative number of events.


PSHA
*********************************************
PSHA with synthetic catalog ...


