Auxiliary Module
################################

The :index:`auxiliary` module contains corollary functions that support the capabilities of the 
platform's core modules (e.g., the source, ground-motion, and site-response modules).
This module, therefore, acts as a bridge between raw data and the functions available in the simulation platform 
by supporting I/O tools, statistical analysis, visualisation, and data management.

Currently, the Auxiliary Module includes functions underpinning the Seismic Source Module 
and its associated case study. 

However, as the project will progress to ground motion and site modules, new functionalities 
will be integrated into this framework. Consequently, this task will remain active throughout 
the project, enabling continuous updates and refinements in response to the platform's evolving 
requirements.

To ensure a structured development process, the module is, for time being, subdivided into 
three primary sub-sections: catalogue processing, statistical tools - plotting, and spatial 
distributions.

Tutorial Contents
-----------------

.. toctree::
   :maxdepth: 1

   ses_processing
