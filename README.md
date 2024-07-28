# Electrowinning for Room-Temperature Ironmaking: Mapping the Electrochemical Aqueous Iron Interface

Data and atomic structures in support of the publication "Electrowinning for Room-Temperature Ironmaking: Mapping the Electrochemical Aqueous Iron Interface", Kavalsky and Viswanathan, *J. Phys. Chem. C.* (2024) (in press)

The repository is organized as follows:

1. [terrace_pourbaix/](terrace_pourbaix)

    * `thermo_data.json`: `json` containing the following quantities for each phase to construct the 110 surface Pourbaix diagram:
    
        * `dG0`: free energy of the surface at 0 V vs SHE and pH = 0
        * `area`: area of the surface in constructing the surface phase in units of per surface atom
        * `ne`: number of electrons produced in forming the phase (ie. -ve is a reduction reaction and +ve is a oxidation reaction)
        * `nH`: number of protons produced in forming the phase (ie. -ve consumes protons and +ve produces protons)
    
    * `{COVERAGE}{ADSORBATE}.traj`: `ase Trajectory` files for the most thermodynamically stable surface phase at `COVERAGE` ML for `ADSORBATE`

2. [step_pourbaix/](step_pourbaix)

    * `step_thermo_data.json`: `json` containing the following quantities for each phase to construct the 210 surface Pourbaix diagram:
    
        * `dG0`: free energy of the surface at 0 V vs SHE and pH = 0
        * `area`: area of the surface in constructing the surface phase in units of per surface atom
        * `ne`: number of electrons produced in forming the phase (ie. -ve is a reduction reaction and +ve is a oxidation reaction)
        * `nH`: number of protons produced in forming the phase (ie. -ve consumes protons and +ve produces protons)
    
    * `{COVERAGE}{ADSORBATE}.traj`: `ase Trajectory` files for the most thermodynamically stable surface phase at `COVERAGE` ML for `ADSORBATE`. **N.B.** All step phases used here have the terrace fully hydrogenated

3. [terrace_deposition/](terrace_deposition)

    * `{NUM_Fe_ATOMS_DEPOSITED}.traj`: `ase Trajectory` files for modeling iron electrodeposition on the 110 terrace with `NUM_Fe_ATOMS_DEPOSITED` deposited on the surface

4. [step_deposition/](step_deposition)

    * `{NUM_Fe_ATOMS_DEPOSITED}.traj`: `ase Trajectory` files for modeling iron electrodeposition on the 210 terrace with `NUM_Fe_ATOMS_DEPOSITED` deposited on the surface

5. [terrace_absorption/](terrace_absorption)

    * `surfaceH.traj`: `ase Trajectory` file of the structure for hydrogen adsorbed on the surface

    * `undershortbridge.traj`: `ase Trajectory` file of the structure for hydrogen buried under the short bridge

    * `hydrogenated_surfaceH.traj`: `ase Trajectory` file of the hydrogenated 110 surface

    * `hydrogenated_undershortbridge.traj`: `ase Trajectory` file for hydrogen buried under the short bridge of a hydrogenated surface

6. [step_absorption/](step_absorption)

    * `understep.traj`: `ase Trajectory` file of the structure for hydrogen buried under the step

    * `beside_step.traj`: `ase Trajectory` file of the hydrogen placed beside the step edge

    * `near_step.traj`: `ase Trajectory` file of the hydrogen placed near the step edge

    * `hydrogenated_understep.traj`: `ase Trajectory` file for hydrogen buried under the step bridge of a hydrogenated surface