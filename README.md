**Introduction**

HighRelax is a novel post-processing strategy that extends the Amber force field to improve the physical realism of protein structures containing non-canonical amino acids (NCAAs). This method, which is designed for use with deep learning protein structure prediction models like AlphaFold3, focuses on restoring stereochemistry, reducing clashes, and refining overall geometry without significantly altering the global conformation.

**Installation**

conda create -n HighRelax python=3.11

conda install -c conda-forge openmm ambertools=25

**Usage**

1、Prepare your input files: Prediction PDB file from AlphaFold3

Force field parameter files (.prepin, .frcmod)

2、Load the structure into tleap: tleap -f leap.in

3、python HighRelax.py 

**Files**

HighRelax.py: Python script to run the HighRelax relaxation.

leap.in: Example input file for tleap to set up the force field and parameters.

test_files/: Example test PDB files and the corresponding output files.

force_field/: Folder containing the .frcmod and .prepin files for NCAAs.
