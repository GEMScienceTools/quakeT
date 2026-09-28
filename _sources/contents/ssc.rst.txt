Seismic Source Module
################################

The *seismic source module* contains instructions and workflows for evaluating 
models related to seismic sources. 

This section outlines how to utilize the **Event-Based PSHA** calculator in 
the `OpenQuake Engine <https://github.com/gem/oq-engine>`_ specifically to generate 
:term:`Stochastic Event Set (SES)`—synthetic catalogues of earthquake ruptures. 

Understanding Event-Based PSHA
==============================

Stochastic Event Set (SES) is a potential realization of the seismicity 
(i.e. a list of ruptures) produced by the source model over the investigation 
time for the hazard calculation. The Event-Based PSHA calculator utilizes Monte Carlo 
sampling :ref:`[16] <ref-musson-1999>` to generate the SES. 

While the standard Event-Based PSHA calculator computes and stores stochastic 
event sets and the corresponding :term:`Ground-Motion Field (GMF)` (often producing hazard 
curves and hazard maps similar to the `Classical PSHA calculator <https://docs.openquake.org/oq-engine/manual/latest/user-guide/workflows/classical-psha.html>`_), **this module 
focuses only on the source generation phase.** The computed synthetic 
catalogues are incredibly valuable for source modeling and can be used directly 
for comparisons against a real catalogue to validate the :term:`seismicity rate` and rupture geometries.

For more detailed information to Event-Based PSHA, please refer to Pagani et al., (2014) :ref:`[17] <ref-pagani-2014>` 
and `OpenQuake Engine Documentation <https://docs.openquake.org/oq-engine/manual/latest/user-guide/outputs/event-based-psha-outputs.html#>`_.

Generating Stochastic Event Sets (SES)
======================================

To generate an SES without computing the subsequent hazard (:term:`Ground-Motion Field (GMF)`), 
we only need to configure the OpenQuake Engine to sample the source :term:`logic tree` and 
generate the temporal and spatial distribution of ruptures.

Inputs
------
All required input files for the event-based calculation is placed within ``data/event_based_PSHA/`` 
folder. Typically, this includes:

* Seismic Source Model XML file (``it_example.xml``).
* Source Logic Tree XML file (``source_model_logic_tree.xml``).
* Main configuration file (``job.ini``).

You can find more detailed information for inputs in the `OpenQuake Engine Documentation <https://docs.openquake.org/oq-engine/manual/latest/user-guide/configuration-file/event-based-psha-config.html>`_.

.. note::
   Because we are exclusively generating earthquake ruptures and skipping the hazard 
   calculation, you **do not** need to provide a Ground Motion Logic Tree (GMM) file or define site models.
   But we keep them in the data folder in case you wish to perform full event-based PSHA.

Simulation phase
----------------
After you prepare the necessary input files of event-based PSHA, you can run the analysis 
and see outputs using your terminal (optional). To do these, there is a plenty of ways 
based on how you use OpenQuake engine. You might see the `Running Calculations 
section <https://docs.openquake.org/oq-engine/manual/latest/getting-started/running-calculations/index.html>`_ for 
running calculations options and more detailed information.

Outputs
------------
At the end of an event-based calculation configured purely for **Stochastic Event Sets generation**, the 
OpenQuake engine will output the generated **Stochastic Event Sets**. The list of outputs  
can be seen using the ``oq engine --lo <calculation ID>`` command. In addition, you can export all the results of a 
given calculation using the ``oq engine --eos <calculation ID> tmp`` for further post-processing and 
comparison against your real catalogues.

.. note::
   In the tutorial section below, you might find how to generate a stochastic event set from an 
   `OQ Engine area source <https://github.com/gem/oq-engine/blob/master/openquake/hazardlib/source/area.py#L25>`_ 
   with known geometry (i.e. a polygon in a shapefile or geojson), 
   a `magnitude-frequency distribution (MFD) <https://github.com/gem/oq-engine/tree/master/openquake/hazardlib/mfd>`_, 
   and a hypocentral depth distribution (optionally specified by means of an `OQ Engine probability 
   mass function <https://github.com/gem/oq-engine/blob/master/openquake/hazardlib/pmf.py#L24>`_).


Tutorial Contents
==================

.. toctree::
   :maxdepth: 1

   mfd_calculation
   ses_generation
   