# GCMC Simulation for FCC System

Welcome to **Molecular Dynamics with Grand Canonical Monte Carlo (GCMC)**!  
This script simulates a molecular system in a face-centered cubic (FCC) lattice using the **Lennard-Jones potential** to model atomic interactions, with the added twist of controlling the chemical potential and density via **GCMC**. So, if you're into simulating materials with fluctuating atom counts (think gas adsorption, phase transitions, or material properties under specific conditions), this is for you! 

### What Does This Simulation Do?

This LAMMPS input script simulates a system of atoms arranged in a face-centered cubic (FCC) lattice and runs a **Grand Canonical Monte Carlo (GCMC)** simulation to control the **chemical potential** and **density** of the system. It includes the following cool features:

- **FCC Lattice Setup**: It starts by setting up a cubic simulation box with a lattice of atoms in an FCC structure.
- **Lennard-Jones Potential**: Lennard-Jones (LJ) potential is used for atomic interactions (you know, the classic attractive-repulsive force between molecules).
- **Grand Canonical Ensemble (GCMC)**: GCMC allows atoms to be inserted and removed during the simulation to maintain a fixed **chemical potential** and **density**.
- **Thermodynamic Monitoring**: Tracks temperature, chemical potential, and atom density through the simulation.

### Features and Key Components

- **Lattice Setup**: 
  - FCC lattice with a lattice constant of `0.1` units.
  
- **Potential and Interactions**:
  - Lennard-Jones potential (`lj/cut` style) with a cutoff distance of `10` units.
  - Lennard-Jones parameters (`epsilon = 0.33`, `sigma = 3.69`) for atom-atom interactions.

- **GCMC Fix**:
  - Grand Canonical Monte Carlo moves are enabled using `fix gcmc`, which controls the chemical potential and density.
  - Atoms are inserted and deleted according to the target chemical potential and temperature.
  
- **Thermodynamics**: 
  - Custom thermodynamic output that tracks step count, atom count, chemical potential, and density.
  - Thermodynamic data is output every `100` steps.

- **Output**:
  - Atomic positions (x, y, z), type, and ID are dumped every `100` steps to a `dump.txt` file for later analysis.

### Key Parameters:
- **Chemical Potential (`chempot`)**: The chemical potential is set to `-2000 kcal/mol` by default.
- **Density Calculation**: The number of atoms is tracked relative to the volume (`atoms/vol`).
- **Temperature**: The temperature is fixed at `300 K` for the simulation.

### How to Run:

1. **Prepare your LAMMPS environment**:  
   Make sure you have LAMMPS installed and properly set up. You can download it from [LAMMPS](https://lammps.sandia.gov/).

2. **Download the Script**:  
   Download or clone this repository with the script and make sure you have the required potential file (like `cu_u3.eam` or any other that fits your system).

3. **Execute the Simulation**:  
   Run the LAMMPS input file using the following command:
   ```bash
   lmp < input_script_name
   ```

4. **Output Files**:
   The output will include a `dump.txt` file that logs the atom IDs, types, and positions at each step.

### Example Output:
- **Step**: 100
- **Atoms**: 1000
- **Chemical Potential**: -2000 kcal/mol
- **Density**: 0.8 atoms/vol

The `dump.txt` will contain atomic data like:
```txt
1000 1 1.0 2.0 3.0
1001 1 2.0 3.0 4.0
...
```

### Why Use This?

- **Control Over Atom Counts**: This simulation type is great for studying systems where the number of atoms fluctuates, such as adsorption processes or molecular interactions in gas-phase simulations.
- **Customizable**: Adjust the lattice constant, chemical potential, and other parameters based on your study needs.
- **Fun and Powerful**: GCMC gives you the flexibility to simulate real-world processes like phase transitions, adsorption, and gas absorption in materials.

### Requirements:
- **LAMMPS**: Make sure you have a working version of LAMMPS installed.
- **EAM Potential File**: If you're simulating metal systems, ensure you have an appropriate **EAM potential file** (like `cu_u3.eam` for Copper).
  
### Final Thoughts:
This script is a great starting point for molecular simulations where atom number fluctuations are key. Whether you’re studying material properties, exploring adsorbates, or analyzing molecular interactions, this script can help you get the job done in style. Just remember: **Credit me if you use it** – let's keep this community thriving. 

Happy simulating! 
