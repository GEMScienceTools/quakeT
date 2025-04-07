.. 
Welcome to the quakeT documentation!
====================================

**quakeT** is an initiative of the SIGMA3 project, jointly conducted by the *Électricité de France (EDF)* and the *GEM Foundation*. 
Its goal is to collect a set of tools for building components of a probabilistic seismic hazard model, 
generating synthetic datasets, and checking the compatibility between observations and models.


quakeT code is hosted on github at the following link: https://github.com/GEMScienceTools/quakeT. 
It is developed in close connection with the `OpenQuake engine <https://github.com/gem/oq-engine>`_ and other toolkits in `GEMScienceTools <https://github.com/GEMScienceTools>`_, 
the open-source hazard and risk calculation engine developed primarily by the GEM Foundation.


Currently the quakeT includes five sub-modules:

* **Auxiliary module** is related to the development of the auxiliary functionalities required to support the modules related to the simulation of each fundamental step of the earthquake process such as pre-simulation, post simulation, and PSHA model with synthetic catalogs;

* **Seismic source module** will contain codes for evaluating models related to seismic sources;

* **Ground motion module** will contain functionalities for computing ground motion intensity measures (IMs);

* **Site and site-effects module** will be developed for modelling the site response;

* **Case study module** will showcase the use of the tools developed within each module in a real case application; 

.. toctree::
   :maxdepth: 2
   :caption: Contents:

   contents/installation
   contents/auxiliary
   contents/ssc
   contents/gmc
   contents/site
   contents/case


Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

