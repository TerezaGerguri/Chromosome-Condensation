# Chromosome-Condensation
A simple biophysical model for chromosome condensation simulations


Table of Contents

•	About ‘Chromo-sim’

•	Getting Started

•	Usage

•	Output & visualization

•	Documentation

•	License

•	Contact

•	Acknowledgements


About ‘Chromo-sim’

‘Chromo-sim’ code is a C++ biophysical software designed for Brownian dynamics of chromatin condensation with two distinct mechanisms – ‘diffusion capture’ which is based on pairwise interactions between chromatin loci or between particles mimicking condensin/cohesin, and ‘loop extrusion’, resulting in formation of chromatin loops. ‘Chromo-sim’ can be also used for simple Brownian dynamics simulations of free polymers without any condensation mechanisms (Yasu’s paper). 
For in-depth description of the model and biophysical algorithms applied, please see https://www.biorxiv.org/content/10.1101/2020.10.15.341305v1.


Getting Started

This is an example of how you may set up the code running for your projects locally.

o	Prerequisites
-	C++ built-in
-	Visualization software such as Chimera, VMD or PyMOL
o	Installation
1.	You can download the code from folder ‘chromo_sim_code’
2.	Or you can clone the repo 
git clone https://github.com/.......


Usage

First, create a folder where you want to run simulations:
mkdir test_sim
cd test_sim

Make sure you copy all the code files from chromo_sim_code to the folder where you want to run simulations:
cp /path_to_code_folder/chromo_sim_code/* ./ 

Next, set up parameters in the initConfig.hpp (for parameter description see ‘Documentation’) and then compile the code:
make

Run the simulation:
./chromo 


Output & visualization

The main output of code are PDB files from specific timepoints with coordinates of polymer and condensin/cohesin proteins.These can be visalized using Chimera, VMD or PyMOL. There are additional output files to monitor further events in the simulations (‘Documentation’) you can opt for. 


Documentation – parameters 

The ‘Chromo-sim’ code consists of several files:

initConfig.hpp = 
initConfig.cpp = 
initDynamics.hpp = 
initDynamics.cpp =  
chromoCell.cpp = 


General parameter set up can be adjusted in initConfig.hpp file, README_parameters.xlsx contains more in-depth description of parameters.

Optional output files and their corresponding parameters are:
•	_chromoPDB_*.pdb = PDB file format of chromatin chain with binders/condensin in selected time point

•	_DC_stats_index2.txt = number of diffusion capture interactions/pairs in time

•	_binder_attach_site.txt = site on chromatin chain where binders are attached
•	_loop_size.txt = loops sizes in time
•	_nested_loops.txt = number of nested loops in time

•	_voxMap_occupancy.txt = number of beads in each voxel
•	_voxMap_occupancy2new.txt = number of occupied voxels

•	_msd_bead_coord.txt = coordinate monitoring in selected time windows, used for further MSD and anisotropy calculations



License
Distributed un the Crick License. See LICENSE for more information.
 

Contact
•	Xiao Fu - @foolbirdie, xiao.fu@crick.ac.uk
•	Tereza Gerguri - @GerguriTereza, tereza.gerguri@crick.ac.uk
•	Paul Bates - @PaulBatesBMM, paul.bates@crick.ac.uk

Acknowledgements

This code was developed under the Biomolecular Modelling Laboratory https://www.crick.ac.uk/research/labs/paul-bates at Francis Crick Institute (https://www.crick.ac.uk/ ) as a part of collaboration with Chromosome Segregation Laboratory https://www.crick.ac.uk/research/labs/frank-uhlmann. 
Please cite our paper (https://www.biorxiv.org/content/10.1101/2020.10.15.341305v1) when using the code.



