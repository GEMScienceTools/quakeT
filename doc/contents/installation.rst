Installation
============
The **QuakeT** is installed with the procedure described in the following. 
Note that this procedure implies the installation of the OpenQuake engine. 
It was tested on **Windows**, **Mac OS** and **Linux** systems.

Here we demonstrate the installation of the QuakeT for a Windows system and Python 3.12.

* Open a terminal and move to the folder where you intend to install the tools;
* Upgrade pip:

.. code-block:: ini

    >python -m pip install --upgrade pip

* Install the OpenQuake engine and activate its virtual environment:

.. code-block:: ini

    >git clone https://github.com/GEMScienceTools/quakeT.git

.. code-block:: ini

    >cd oq-engine

.. code-block:: ini

    >python3 install.py devel

.. code-block:: ini

    >openquake/script/activate

* Go to the folder where you cloned the QuakeT repository and complete the installation running the following commands, making sure to replace `requirements.txt` with the name of the file corresponding to the correct python version and operating system:

.. code-block:: ini
    
    >pip install -e .

.. code-block:: ini
        
    >pip install -r requirements.txt
