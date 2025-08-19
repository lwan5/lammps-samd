Note:

In the tarball 'lammps-samd.rar', a patch file implementing SAMD functionality in official LAMMPS releases, a set of LAMMPS input scripts for reproducing the results in Fig. 3, and a documentation detailing file usage and implementation procedures are provided.

Usage of the patch file:

Go to the root of your LAMMPS directory, copy the patch file to this directory, then type the following command in console:

patch -p1 < patch_samd_to_lammps_2Apr2025

If successful, one can then compile the lammps source code as usual. Normally you don't have change anything in the makefile.

In the 'example' folder, the lammps input scripts are given for reproduction of the results in Fig. 3 of the SAMD article. Simply run these scripts by the newly generated lammps executable in the following order:

in.Fe-28C.min (Construction of the model & then do structural relaxation by minimization at 0 K.)

in.Fe-28C.init (Get the equilibrium state of the model at 750 K and zero stress.)

in.Fe-28C.samd (Do SAMD running of the model at 750 K and calculate the diffusion distance of carbon atoms.)

Contact: lwan5@outlook.com (Liang WAN)
