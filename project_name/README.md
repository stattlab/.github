The README file should document the project data and workflow. Please follow a variation of
the template below, and write using reStructuredText or Markdown. The following example is from a recent project that uses reStructuredText:

=======================
MPCD in Channels
=======================
Authors: Tzortzis Koulaxizis (tk16@illinois.edu), Antonia Statt

This project simulates dilute polymer chains in various channel geometries, using MPCD as solvent. 
(other high level information goes here) 

This project uses hoomd 4.8.0, signac 2.0, numpy, ... 

Directory contents
==================
* ``bmark``: Preliminary benchmarks of delta nodes.
* ``diffusion``: Equilibrium (diffusion) simulations.
The structure of the diffusion directory is ``lambda_X/phi_Y/Z``,
where ``X`` is the aspect ratio, ``Y`` is the volume fraction, and
``Z`` is the replica number. Each directory contains the following
important outputs:
- ``trajectory_all.gsd``: snapshots of all particles in the simulation.
- ``trajectory_polymer.gsd``: snapshot of just polymers  (This file may be deleted to save disk
space once postprocessing is complete.)
- ``msd.dat``: the mean-squared displacement (MSD) of the trajectory.
Additionally, a file ``average_msd.dat`` in each ``phi_Y`` directory contains
the average MSD from each replica with estimated error.
.... 
(describe all folders/files) 


Workflow steps
==============
1. Run ``init.py``. This script is idempotent, initializes signac workspace 
2. Run ``project.py`` ...
3. Submit the jobs with the script `project.py`` (explain more detail)
4.  Once all replicas are finished, run XX to compute
the MSD and average results together. (explain more detail)
5. ... 
