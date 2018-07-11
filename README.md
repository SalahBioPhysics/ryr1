# ryr1
For an overview on the ryanodine receptor (RyR1) being a Ca+2 channel that facilitates skeletal muscle excitation and contraction, we can refer to this [paper](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5142848/).

In this project, we are calculating the energy landscapes using Multi-Conformer Continuum Electrostatics ([MCCE])(https://sites.google.com/site/mccewiki/home). Calculations are done with two datasets.  One set involves the RyR1 macromolecules in equilibrium with a thermal bath sans the activation of ligands; the other involves the RyR1 macromolecules in equilibrium with both a thermal bath as well as a reservoir of the activated ligands calcium, ATP, and caffeine. 

## ligand_binding_sites:
These PDB files were prepared by Danya Ben Hail.  There are 50 files labeled frame_01 to frame_50.  The structure of this data set is modified such that only residues near the binding site are calculated. Each frame_0i directory contains an input pdb, here highlighted in black. 

![ryr1(blue). Input pdb(black)](presentation/img01.png)

The generated output files are titled head3.lst and fort.38. 
## head3.lst
* iConf:conformer ID
* CONFORMER: conformer name
* FL: flag| f means the conformer is on, t means the conformer is off.
* occ: occupancy
* crg: charge
* Em0: Em in solution
* pKa0: pka in solution
* ne: # of electrons
* nH: # of protons
* vdw0: self vdW energy + implicit vdW energy (favorable) with solvent (water)
* vdw1:backbone vdW
* tors: torsion energy
* epol: backbone electrostatic interaction
* dsolv: desolvation energy 
* extra: extra energy term (This is the value we change when we want to calculate titration curve for the ligand)
* history: to keep track of the conformer

## fort.38
This file shows the occupancy of each conformer at differernt ph/eh/ch values.  In our case, we are using chemical titration (ch). The plot below shows the Ca+2 titration carve of frame01.
![Ca+2 titration carve](presentation/CADMG5104_002.png) 


 
