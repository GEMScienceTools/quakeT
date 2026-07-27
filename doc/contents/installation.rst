Installation
################################

This guide covers the necessary steps to set up your environment for the **Simulation Platform**. You will need to install Python dependencies and system-level tools like the Generic Mapping Tools (GMT) :ref:`[2] <ref-wessel-2019>`.
Also, the tutorials rely on the `OpenQuake engine <https://github.com/gem/oq-engine>`_ and `OpenQuake Model Building Toolkit (oq-mbtk) <https://github.com/GEMScienceTools/oq-mbtk/tree/master>`_. Before proceeding, you must have ``OpenQuake engine`` and ``oq-mbtk`` installed.

Here we demonstrate the installation of the QuakeT and its necessary dependencies, respectively. 

Get the QuakeT Source Code
==========================

Open a terminal and move to the folder where you intend to install the tools;

Clone the repository using the `web URL of QuakeT repository: <https://github.com/GEMScienceTools/quakeT.git>`_

.. code-block:: bash

    git clone https://github.com/GEMScienceTools/quakeT.git

Go to the folder where you cloned the QuakeT repository and make it in “editable” mod running the following command:

.. code-block:: bash

    pip install -e .

OpenQuake engine Setup
======================
Please follow the official installation instructions of **OpenQuake Engine** here:
`OpenQuake engine Installation Guide. <https://docs.openquake.org/oq-engine/manual/latest/getting-started/index.html#getting-started>`_

OpenQuake MBTK Setup
====================
Please follow the official installation instructions of **oq-mbtk** here:
`OpenQuake MBTK Installation Guide. <https://gemsciencetools.github.io/oq-mbtk/contents/installation.html>`_

Python Environment Setup
========================

It is highly recommended to use a virtual environment (conda or venv) to avoid dependency conflicts.

.. code-block:: bash

    # Create and activate a virtual environment (optional)
    python -m venv quaket_env
    source quaket_env/bin/activate  # On Windows: quaket_env\Scripts\activate

    # Install Python libraries
    pip install pandas geopandas shapely matplotlib ipython

System Requirements
===================

The spatial distribution tutorials require **GMT** to be installed on your operating system.

macOS
-----

The easiest way to install these tools on macOS is using `Homebrew <https://brew.sh/>`_:

.. code-block:: bash

    brew install gmt

Windows
-------

1. **GMT:** Download and run the executable installer (.exe) from the `GMT Official Releases <https://www.generic-mapping-tools.org/download/>`_. During installation, ensure you check the box **"Add GMT to the system PATH"**.
2. **Ghostscript:** (Required by GMT for PNG output) Download and install from the `Ghostscript site <https://ghostscript.com/releases/gsdnld.html>`_.

Linux
-------

Use the package manager to install the required tools:

.. code-block:: bash

    sudo apt update
    sudo apt install gmt gmt-dcw gmt-gshhg

Verification
============

After installation, verify that the tools are correctly set up by running these commands in your terminal or command prompt:

.. code-block:: bash

    gmt --version

.. note::
   If you receive a "command not found" error, you may need to restart your terminal or manually add the installation folders to your system's Environment Variables (PATH).