# FCC Metal Simulation with Style 

Welcome to **THE** LAMMPS input script you didn’t know you needed! Dive into a sleek simulation of FCC copper atoms that’s as scientifically accurate as it is effortlessly cool. Use it, tweak it, love it — just don’t forget to give me credit. 

---

## **What’s Inside?**
This script sets up a molecular dynamics (MD) simulation of an FCC lattice with some spicy layered dynamics. Think thermodynamic elegance, velocity tricks, and top-tier atom shuffling. 

### **Highlights**:
1. **Copper Wonderland**:
   - Face-Centered Cubic (FCC) lattice with a 3.61 Å magic touch. 
   - Region dimensions: `15 x 15 x 20` (because who doesn’t love symmetry?).

2. **Region Drama**:
   - **Region v**: The bulk playground.
   - **Region n**: A spherical void—because sometimes you just want to delete atoms for fun.
   - **Region s**: A solid foundation with layers (`f`, `t`, `m`) each doing their own thing. It's like the lasagna of MD.

3. **Dynamic Shenanigans**:
   - **NVT for region s**: Stable and chill at 300 K.
   - **NVE in region m**: Letting loose with energy conservation.
   - **Velocity magic for n**: A void on the move. 
   - And region `f`? Fixed in place like that one friend who never dances.

4. **Force Field Hybrid**:
   - Embedded Atom Method (EAM) for metallic realism.
   - Lennard-Jones for cross-type interactions because #diversity.

5. **Sick Outputs**:
   - Atomic coordinates saved in style (`dump.txt` every 100 steps).
   - Thermo data? Oh, it’s custom, baby. We log what *you* need.

---

## **How to Slay This Simulation**
1. Clone this masterpiece:
   ```bash
   git clone https://github.com/username/FCC-Metal-Simulation.git
   cd FCC-Metal-Simulation
   ```

2. Unleash the atoms in LAMMPS:
   ```bash
   lmp_mpi -in in.simulation
   ```

3. Marvel at the results:
   - Load `dump.txt` in OVITO, VMD, or anything cool enough for your vibes.
   - Peek at the thermodynamics and flex about it to your friends.

---

## **What’s in the Bag?**
- **`in.simulation`**: The brain of this operation. Our hero.
- **`cu_u3.eam`**: Copper’s personal trainer. All those interactions? Yep, that’s this file.
- **`dump.txt`**: Your atomic gossip column. All the positions, all the drama.

---

## **Use It. Love It. Credit Me.**
This project is open, free, and fabulous. You can:
- Use it for your simulations.
- Modify it to fit your wildest MD dreams.
- Brag about it in your papers, projects, or Nobel acceptance speech.

Just drop my name somewhere:
**[Reyrove]**

No credit? No chill.  

Enjoy, and may your atoms always find their perfect neighbors! 
