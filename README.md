# Overview
This code is designed to simulate Coble creep deformation and void nucleation/growth in a 3D polycrystalline solid.

# Requirements
* [**Neper**](https://neper.info/index.html): This is required to generate an arbitrary polycrystalline structure in a representative volume element (RVE).
  * Official releases can be obtained from the [GitHub repository](https://github.com/neperfepx/neper).
  * A Unix-like system is necessary to run Neper. For Windows OS, you can use Windows Subsystem for Linux (WSL).
  * Detailed information about Neper is available [here](https://neper.info/index.html).
 
* [**Python 3.10**](https://www.python.org/downloads/): This is necessary for running the simulation.
  * Additionally, the following libraries are required: Pandas, NumPy, Math, JSON, Random, SymPy, Scipy, and Workbook. You can install these libraries using the following commands:
    `pip install pandas numpy math jsonlib random sympy scipy Workbook`

# How to Execute
1. Generate the **polycrystal.tess** file using the Neper Tessellation Module.
   * The **polycrystal.tess** file includes all the data describing the polycrystalline structure.
   * We have provided a sample file for your convenience.
2. Modify the values in the **parameters.dat** file.
   * The **parameters.dat** file includes all the required input parameters other than the data describing the polycrystalline structure, such as the target temperature, applied stress tensor, material constants, and numerical conditions.
3. Place **polycrystal.tess**, **parameters.dat**, and **creep.py** in the same directory, and execute **creep.py**. The strain and void area fraction data will be exported in the output file named **results.dat**. If you wish to extract other data evaluated in the simulation, you can do so by making slight modifications to **creep.py**.
