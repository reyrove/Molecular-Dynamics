# FCC Simulations Collection

Welcome to the ultimate **FCC Simulations Collection**! This is your one-stop shop for some seriously awesome LAMMPS simulations. Whether you're into **copper deposition**, **metal interactions**, or playing around with **Grand Canonical Monte Carlo (GCMC)** simulations, this repo's got you covered. So grab your coffee (or something stronger), and let's dive into the world of FCC lattice systems.

## What’s Inside? 

### 1. **FCC Copper Deposition Simulation**  
**Copper, baby!** Watch those copper atoms fall like they’re the hottest thing on the block. We’re simulating the process where copper atoms are deposited onto an FCC lattice. Expect a smooth, steady interaction using the **EAM potential**—because nothing says "metal" like copper.

- **What you get**:
  - FCC lattice with copper atoms (yeah, it’s shiny)
  - **EAM potential** for those copper vibes
  - Periodic boundary conditions for that *infinite* feel
  - Temperature control to keep it cool, always

### 2. **FCC Metal Simulation with Style**  
Who said metal can’t be stylish? This is where we bring in **hybrid potentials** and control the temperature like we’re wearing a leather jacket in winter. With **EAM** and **Lennard-Jones** potential, it’s not just any metal system; it’s a showstopper.

- **What you get**:
  - FCC lattice with some serious style (hybrid EAM + Lennard-Jones potential)
  - **Nose-Hoover thermostat** to keep things temperature-appropriate
  - Customizable pair interactions because we like it personal
  - Periodic boundaries, because why not?

### 3. **GCMC Simulation for FCC Lattice**  
Okay, so maybe you’ve got some gas molecules and you need to know how they *react* with that solid FCC lattice. This is your jam. We’re using **Grand Canonical Monte Carlo (GCMC)** to simulate adsorption and desorption processes like a pro. Control that **chemical potential** like you own it.

- **What you get**:
  - GCMC goodness with an FCC lattice
  - Adsorption/desorption magic happening in real time
  - Controlled **chemical potential** (because you’re the boss)
  - Periodic boundaries—again, infinite feels

### 4. **GCMC Simulation for FCC System**  
Take the GCMC skills you learned and bring them to any FCC system you want. From gases interacting with surfaces to some serious material science, this script is ready for action. If you want to control **particle densities** and **chemical potential**, this is your stage.

- **What you get**:
  - Generalized GCMC action for any FCC system you need
  - Flexible, because you're a multitasker
  - Control over particle densities—**it’s your universe**
  - Periodic boundaries, because everything goes on forever

## How to Use This Like a Pro 

1. **Clone this repo** to your local machine. It’s as easy as:
   ```
   git clone https://github.com/yourusername/FCC_Simulations.git
   ```

2. **Navigate to the folder** for the simulation you want to run.  
   Example:  
   ```
   cd FCC_Simulations/FCC_Copper_Deposition_Simulation
   ```

3. **Run the LAMMPS simulation**. You’re basically running science here:
   ```
   lmp < copper_deposition.in
   ```
   (Make sure you've got LAMMPS set up, or you’ll be out of luck)

4. **Peep your results** in the **`results/`** folder. The output files will include dumps, logs, and anything else that might make your heart race.

## Requirements 

- **LAMMPS**: If you don’t have it yet, what are you even doing? Install it, configure it, and make sure it works because you’re about to simulate some serious stuff.
- **Potential Files**: You might need some extra files, like `cu_u3.eam` for copper, so make sure you’ve got them in the right spot (or point to them in the input script).

## License 

This is **free to use**, modify, and do whatever you want with—**as long as you give credit**. Just don’t forget to shout out where you got this from if you decide to use or redistribute any part of this repo. Simple enough, right? 

---

### Contributing 

Wanna contribute? Go ahead, fork this thing, make it better, or just improve the docs! If you find a bug or something’s broken, **let us know**—don’t leave us hanging.

---

### Acknowledgments 

We’ve gotta shout out the creators and maintainers of **LAMMPS**. Seriously, they’re the real MVPs. Also, credit to everyone who’s made the potentials and methods in this repo work so well!

---

There you go—simulations, sass, and all the info you need to make your material science simulations *pop*. Go ahead and make some magic happen.

