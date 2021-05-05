# ChainswQEs
This folder contains eigenvectors and eigenenergies for two quantum emitters dipole coupled to each end of an atom chain with interacting electrons.  The files for vectors and energies that should go together have a matching naming scheme.

The folder GarnettsRunsOrdered contains files from the directory /home/garnettb/quantum_plasmonics/12_6_cn_full_exch0.2_2qe_1.00c_1.00dip_vary_eqe/
A sample output file gives the parameters used by the code, except that each run in this directory varies by the energy difference between the ground and excited state of the quantum emitters (qubit) on each end of the chain.  The plasmon excitation on the chain has an energy (I believe) of 0.595 (in units of the hopping, which we set as one).  So the files that end in 0.595eqe are for the case where the emitters are resonant with the chain.  The others are not resonant.

The folder EmilysRunsDisordered contains files from the directory /home/etownsen/quantumplasmonics/runs/newerRuns/Disorder/1by12w6Dis2QE/seed1/
These runs have disorder in the placement of the atoms, which can affect the hopping between two neighboring sites, and the Coulomb interaction between pairs of electrons.  Whether or not the disorder affects these terms of the Hamiltonian is indicated by yesH or noH (if it affects the hopping) and yesC or noC (if the disorder affects the Coulomb interaction).  I've included the case noH_noC, which should be nearly the same as Garnett's resonant case. (The disorder will slightly affect the dipole coupling with the emitters, so it might be very slightly different.)  All of these runs are done with the quantum emitters resonant with the lowest energy excitation of the chain.  However that excitation is not as plasmonic anymore once there is enough disorder, and the energy of that excitation changes with disorder.  

I included two cases where the disorder affects both the hopping and the Coulomb interaction.  In the first case there is small disorder (0.01Da_0.05Db, which means that there is a variation in the position of the atoms that is 1% of a lattice spacing in the direction perpendicular to the chain and a 5% variation in the direction along the chain).  In the second case there is large disorder (0.01Da0.30Db).
These runs are all from the same random seed that is used to add the disorder.  
Emily Townsend 
5/5/2021

ls GarnettsRunsOrdered
energy_12_6_-1.0t_-0.5n_1.00c_0.0e_2qe_0.40eqe
energy_12_6_-1.0t_-0.5n_1.00c_0.0e_2qe_0.50eqe
energy_12_6_-1.0t_-0.5n_1.00c_0.0e_2qe_0.595eqe
out_diag_12_6_-1.0t_-0.5n_1.00c_0.0e_2qe_0.595eqe_1.00dip
vectors_12_6_-1.0t_-0.5n_1.00c_0.0e_2qe_0.40eqe
vectors_12_6_-1.0t_-0.5n_1.00c_0.0e_2qe_0.50eqe
vectors_12_6_-1.0t_-0.5n_1.00c_0.0e_2qe_0.595eqe

ls EmilysRunsDisordered
energy1by12w6_0ta_-1tb_-0.5n_1c_0.2ex_0.2Lhop_noH_noC_0.01Da_0.05Db_EQE0.595
energy1by12w6_0ta_-1tb_-0.5n_1c_0.2ex_0.2Lhop_yesH_yesC_0.01Da_0.05Db_EQE0.641
energy1by12w6_0ta_-1tb_-0.5n_1c_0.2ex_0.2Lhop_yesH_yesC_0.01Da_0.30Db_EQE0.248
out1by12w6e2qe0ta-1tb-0.5n1c0.2ex0.2LhopnoHnoC0.01Da0.05Db0.595Eqe1
vect_1by12w6_0ta_-1tb_-0.5n_1c_0.2ex_0.2Lhop_noH_noC_0.01Da_0.05Db_EQE0.595
vect_1by12w6_0ta_-1tb_-0.5n_1c_0.2ex_0.2Lhop_yesH_yesC_0.01Da_0.05Db_EQE0.641
vect_1by12w6_0ta_-1tb_-0.5n_1c_0.2ex_0.2Lhop_yesH_yesC_0.01Da_0.30Db_EQE0.248
