**FCC Copper Deposition Simulation**

## Overview

Ready to unleash some atomic-level chaos? This script simulates an **FCC copper system** using LAMMPS, complete with **atom deposition**, **temperature control**, and **vacancy creation**. Whether you’re messing with material properties or just curious about molecular dynamics, this input file’s got you covered.

---

## Features

- **FCC Copper Lattice**: Creating the ultimate copper playground with a lattice constant of 3.61 Å. Go ahead, break it.
- **Vacancy Creation**: Deleting atoms from a spherical region for some good ol' vacancy shenanigans.
- **Atom Deposition**: Watch as copper atoms crash into the simulation box like they own the place.
- **Langevin Thermostat**: Keeping things chill at 300 K with some Langevin dynamics. No wild temperature swings here.
- **Hybrid Potentials**: EAM for copper and LJ for cross-atom interactions. Smooth.
- **Thermo Data**: Keep track of your system’s temperature every 1000 steps like a boss.

---

## Requirements

- **LAMMPS**: Install it from [here](https://lammps.sandia.gov/download.html) if you don’t already have it.
- **Potential File**: You’ll need the `cu_u3.eam` file for copper. Make sure it’s in the same folder or point to it in the script.

---

## How to Run

1. **Clone the Repo**:
    ```bash
    git clone https://github.com/your-username/fcc-copper-simulation.git
    cd fcc-copper-simulation
    ```

2. **Make Sure LAMMPS is Installed**:
    If you haven't already, grab LAMMPS from the [official site](https://lammps.sandia.gov/download.html).

3. **Run the Script**:
    Launch your simulation with:
    ```bash
    lmp_mpi -in in.simulation
    ```

4. **Check Your Output**:
    - **`dump.txt`**: Atomic data (IDs, types, coordinates) saved every 1000 steps. Perfect for tracking the madness.
    - Thermo data like temperature will pop up every 1000 steps in the terminal. Keep it cool.

---

## Input Script Breakdown (`in.simulation`)

1. **Initialization**: Sets up the system with a metal unit style and a basic FCC copper lattice. No fuss.
2. **Region & Groups**: We define regions for atom deletion (vacancies) and control which atoms get affected. Bye-bye atoms.
3. **Atom Deposition**: Copper atoms are shot into the box with a velocity, filling up the region like it's rush hour.
4. **Temperature Control**: Langevin dynamics for steady temperature (300 K). Chill vibes only.
5. **Fixes & Computations**: All the physics happening behind the scenes, from atom motion to temperature calculation.
6. **Thermo Output**: Tracks temperature, outputs data every 1000 steps. No drama, just data.

---

## Notes

- **File Paths**: Make sure your `cu_u3.eam` potential file is in the same directory as the script. If not, update the path. Simple.
- **LAMMPS Version**: Ensure you're using a version that supports all the cool stuff in this script (like `fix deposit`).
- **Simulation Box**: It's a 10x10x10 box. You can tweak it, but this setup gets the job done for most basic tests.

---

## License

Feel free to use it for whatever, just **credit me** if you’re publishing or sharing. It's free, but don't be shady. Contributions are welcome!

---

## Contact

If you run into issues, have questions, or want to make this even cooler, hit me up on GitHub.

**Author**: [ReyRove]  
**GitHub**: [Your GitHub Profile](https://github.com/reyrove)  

---

Run wild with those atoms and let me know how it goes! 
