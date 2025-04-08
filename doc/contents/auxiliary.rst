Auxiliary module
################################

The :index:`auxiliary` module contains functionalities for preparing input and processing outputs of various simulations.

In particular, it provides:

- Tools for preparing the input to MCQsim and post-processing the output.

Pre-simulation
*********************************************

The pre-simulation tool focuses on preparing and managing input information.
Its core functionalities include:

- **Fault information management**: 
  Import and modify fault segment data stored in GeoJSON format, including geometrical and attribute handling;

- **Geometry validation**: 
  Check and validate the geometric consistency of fault segments to ensure accurate meshing and simulation;

- **Triangular meshing**:
  Generate triangular meshes based on the fault geometry, enabling detailed structural representation;

- **STL file creation**:
  Convert the meshed fault segments into STL (Stereolithography or Standard Triangle Language) file format, 
  suitable for 3D visualization and numerical simulations;


Post simulation
*********************************************

The post-simulation tool focuses on processing output results.
Its core functionalities include:

- **Catalog processing**: 
  Load catalogue as a `.mat` file and save it as a `.csv` file;

- **Statistical evaluation**: 
  Compute statistics for magnitude, rupture area, mean slip, and mean stress drop;

- **3D spatial visualization**: 
  Visualize spatial distribution of events;

- **Magnitude-frequency distribution (MFD)**: 
  Generate MFDs of the simulated earthquake catalogue;


PSHA
*********************************************


