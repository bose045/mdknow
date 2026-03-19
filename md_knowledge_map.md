# Molecular Dynamics & Molecular Simulations — Knowledge Map

> A living reference covering theory, methodology, and software implementation.
> Each topic is a placeholder for short notes on theory and implementation.

---

## Table of Contents

1. [Theoretical Foundations](#1-theoretical-foundations)
2. [Force Fields & Potential Energy Functions](#2-force-fields--potential-energy-functions)
3. [Long-Range Electrostatics](#3-long-range-electrostatics)
4. [Integration Algorithms](#4-integration-algorithms)
5. [Thermostats & Barostats](#5-thermostats--barostats)
6. [Enhanced Sampling Methods](#6-enhanced-sampling-methods)
7. [Free Energy Calculations](#7-free-energy-calculations)
8. [Coarse-Grained & Multiscale Methods](#8-coarse-grained--multiscale-methods)
9. [QM/MM Methods](#9-qmmm-methods)
10. [Analysis & Observables](#10-analysis--observables)
11. [System Preparation](#11-system-preparation)
12. [MD Software & Implementation](#12-md-software--implementation)
13. [Machine Learning & AI-Driven MD](#13-machine-learning--ai-driven-md)
14. [Special System Types](#14-special-system-types)
15. [Performance & HPC](#15-performance--hpc)
16. [Monte Carlo Methods](#16-monte-carlo-methods)
17. [Validation, Reproducibility & Best Practices](#17-validation-reproducibility--best-practices)

---

## 1. Theoretical Foundations

### 1.1 Classical Mechanics & Equations of Motion

- [ ] Newton's equations of motion
- [ ] Lagrangian mechanics
- [ ] Hamiltonian mechanics
- [ ] Phase space & Liouville's theorem
- [ ] Ergodic hypothesis
- [ ] Time reversibility & microreversibility
- [ ] Equipartition theorem
- [ ] Virial theorem

### 1.2 Statistical Mechanics

- [ ] Microcanonical ensemble (NVE)
- [ ] Canonical ensemble (NVT)
- [ ] Isothermal-isobaric ensemble (NPT)
- [ ] Grand canonical ensemble (μVT)
- [ ] Gibbs ensemble
- [ ] Partition function & free energy
- [ ] Fluctuation theorems (Jarzynski, Crooks)
- [ ] Linear response theory
- [ ] Green-Kubo relations
- [ ] Fluctuation-dissipation theorem

### 1.3 Thermodynamics

- [ ] Thermodynamic potentials (U, H, A, G)
- [ ] Maxwell relations
- [ ] Legendre transforms
- [ ] Equation of state
- [ ] Phase transitions & coexistence
- [ ] Chemical potential

---

## 2. Force Fields & Potential Energy Functions

### 2.1 Bonded Interactions

- [ ] Bond stretching (harmonic, Morse, anharmonic)
- [ ] Angle bending
- [ ] Proper dihedral (torsion) potentials
- [ ] Improper dihedrals (out-of-plane bending)
- [ ] Urey-Bradley terms
- [ ] Cross terms (CMAP, stretch-bend)
- [ ] 1-2, 1-3, 1-4 exclusions

### 2.2 Non-Bonded Interactions

- [ ] Lennard-Jones 12-6 potential
- [ ] Buckingham potential
- [ ] Electrostatics & Coulomb interactions
- [ ] van der Waals interactions
- [ ] Mixing rules (Lorentz-Berthelot, geometric)
- [ ] Non-bonded cutoffs & switching functions
- [ ] Tail corrections

### 2.3 Biomolecular Force Fields

- [ ] CHARMM (c22, c27, c36, c36m)
- [ ] AMBER (ff94, ff99SB, ff14SB, ff19SB)
- [ ] OPLS-AA / OPLS3e / OPLS4
- [ ] GROMOS (43A1, 53A6, 54A7)
- [ ] AMOEBA (polarizable)
- [ ] Drude oscillator model
- [ ] MARTINI (coarse-grained)
- [ ] SIRAH (coarse-grained)
- [ ] PRIME20 (protein CG)
- [ ] Force field validation strategies

### 2.4 Small Molecule & Materials Force Fields

- [ ] GAFF / GAFF2 (AMBER)
- [ ] CGenFF (CHARMM general)
- [ ] OPLS-AA for small molecules
- [ ] DREIDING
- [ ] UFF (universal)
- [ ] ReaxFF (reactive)
- [ ] INTERFACE force field
- [ ] Metal force fields (EAM, Finnis-Sinclair)
- [ ] Coarse-grained polymer FFs
- [ ] Polarizable force fields (AMOEBA, Drude, FQ)

### 2.5 Water Models

- [ ] SPC
- [ ] SPC/E
- [ ] TIP3P
- [ ] TIP4P / TIP4P-Ew / TIP4P/2005
- [ ] TIP5P
- [ ] OPC / OPC3
- [ ] SPCE/X
- [ ] Implicit solvent models (GB, PB)
- [ ] Polarizable water models (SWM4-NDP)

### 2.6 Force Field Parameterization

- [ ] QM reference data (HF, MP2, DFT)
- [ ] Charge derivation (RESP, AM1-BCC)
- [ ] Torsion scanning & fitting
- [ ] Paramfit / FFTK / CGenFF program
- [ ] ForceBalance
- [ ] Machine learning FF fitting
- [ ] Transferability & validation

---

## 3. Long-Range Electrostatics

### 3.1 Periodic Boundary Conditions (PBC)

- [ ] Minimum image convention
- [ ] PBC in triclinic boxes
- [ ] Ewald summation
- [ ] Particle mesh Ewald (PME)
- [ ] Smooth PME (SPME)
- [ ] Particle-particle particle-mesh (P3M)
- [ ] Fast multipole method (FMM)
- [ ] Reaction field method
- [ ] Wolf summation
- [ ] Isotropic periodic sum (IPS)

### 3.2 PBC Artifacts & Corrections

- [ ] Finite size effects
- [ ] Charged system corrections
- [ ] Anisotropy in PME
- [ ] Net charge corrections
- [ ] Pressure artifacts in charged systems

---

## 4. Integration Algorithms

### 4.1 Core Integrators

- [ ] Verlet algorithm
- [ ] Leapfrog algorithm
- [ ] Velocity Verlet
- [ ] Beeman algorithm
- [ ] Runge-Kutta methods
- [ ] Symplectic integrators
- [ ] RESPA / r-RESPA (multiple time-stepping)
- [ ] Reversibility & conservation properties

### 4.2 Constraints & Rigid Bodies

- [ ] SHAKE algorithm
- [ ] LINCS algorithm
- [ ] SETTLE (rigid water)
- [ ] Holonomic constraints
- [ ] CCMA (constraint matrix)
- [ ] Rigid body integrators
- [ ] Rigid segment integration

### 4.3 Time Step Selection

- [ ] Nyquist criterion for bond vibrations
- [ ] Hydrogen mass repartitioning (HMR)
- [ ] Adaptive time stepping
- [ ] Virtual sites for extended time steps

---

## 5. Thermostats & Barostats

### 5.1 Thermostats

- [ ] Velocity rescaling
- [ ] Berendsen thermostat
- [ ] Andersen thermostat
- [ ] Nosé-Hoover thermostat
- [ ] Nosé-Hoover chains
- [ ] Langevin thermostat
- [ ] Stochastic velocity rescaling (V-rescale)
- [ ] Bussi-Donadio-Parrinello
- [ ] Dissipative particle dynamics (DPD) thermostat
- [ ] Lowe-Andersen thermostat

### 5.2 Barostats

- [ ] Berendsen barostat
- [ ] Parrinello-Rahman barostat
- [ ] Monte Carlo barostat
- [ ] Andersen barostat
- [ ] MTTK (Martyna-Tobias-Klein)
- [ ] C-rescale barostat
- [ ] Isotropic vs. anisotropic pressure coupling
- [ ] Semi-isotropic pressure coupling (membranes)
- [ ] Compressibility settings

---

## 6. Enhanced Sampling Methods

### 6.1 Collective Variable (CV)-Based

- [ ] Umbrella sampling
- [ ] Weighted histogram analysis method (WHAM)
- [ ] Adaptive biasing force (ABF)
- [ ] Metadynamics (standard)
- [ ] Well-tempered metadynamics
- [ ] Parallel-bias metadynamics
- [ ] Funnel metadynamics
- [ ] Adaptive metadynamics
- [ ] Extended adaptive biasing force (eABF)
- [ ] CZAR estimator
- [ ] OPES (On-the-fly probability enhanced sampling)
- [ ] Steered MD (SMD)
- [ ] Jarzynski equality applications
- [ ] TAMD / d-AFF

### 6.2 Replica-Based Methods

- [ ] Replica exchange MD (REMD / HREMD)
- [ ] Temperature REMD (T-REMD)
- [ ] Hamiltonian REMD (H-REMD)
- [ ] Solute tempering (REST2)
- [ ] REST (replica exchange with solute tempering)
- [ ] Gibbs ensemble Monte Carlo
- [ ] Multi-dimensional REMD

### 6.3 Accelerated Dynamics

- [ ] Hyperdynamics
- [ ] Bond-boost method
- [ ] Accelerated MD (aMD)
- [ ] Gaussian-accelerated MD (GaMD)
- [ ] Targeted MD
- [ ] Conformational flooding
- [ ] String method
- [ ] Transition path sampling (TPS)
- [ ] Forward flux sampling (FFS)
- [ ] Milestoning
- [ ] MFPT estimation
- [ ] Weighted ensemble (WE)
- [ ] WESTPA framework
- [ ] Adaptive sampling

### 6.4 Path-Based & Rare Event Methods

- [ ] Nudged elastic band (NEB)
- [ ] Finite temperature string method
- [ ] Transition interface sampling (TIS)
- [ ] Partial path TIS (PPTIS)
- [ ] Swarm of trajectories
- [ ] Boxed MD
- [ ] Aimless shooting

---

## 7. Free Energy Calculations

### 7.1 Alchemical Methods

- [ ] Thermodynamic integration (TI)
- [ ] Free energy perturbation (FEP)
- [ ] Bennett acceptance ratio (BAR)
- [ ] Multistate BAR (MBAR)
- [ ] Replica exchange perturbation
- [ ] λ-dynamics
- [ ] Soft-core potentials
- [ ] Decoupling vs. annihilation
- [ ] Dual topology vs. single topology
- [ ] Solvation free energy
- [ ] Binding free energy (RBFE, ABFE)
- [ ] Alchemical transfer method (ATM)

### 7.2 Potential of Mean Force (PMF)

- [ ] Umbrella sampling + WHAM
- [ ] ABF-based PMF
- [ ] Metadynamics FES reconstruction
- [ ] Histogramming methods
- [ ] MBAR-based PMF
- [ ] 2D/multi-dimensional PMF

### 7.3 End-Point Methods

- [ ] MM-PBSA
- [ ] MM-GBSA
- [ ] LIE (linear interaction energy)
- [ ] Solvation corrections
- [ ] Normal mode entropy
- [ ] NMODE analysis

---

## 8. Coarse-Grained & Multiscale Methods

### 8.1 CG Model Development

- [ ] MARTINI 2 / MARTINI 3
- [ ] SIRAH force field
- [ ] SDK (Shinoda-DeVane-Klein)
- [ ] PRIME20 for proteins
- [ ] Elastic network models (ENM)
- [ ] Anisotropic network model (ANM)
- [ ] Go-like models
- [ ] Structure-based models
- [ ] Iterative Boltzmann inversion (IBI)
- [ ] Force-matching (multiscale coarse-graining)
- [ ] Relative entropy minimization

### 8.2 Multiscale Approaches

- [ ] QM/MM (ONIOM, AMBER/Gaussian)
- [ ] QM/MM boundaries & link atoms
- [ ] Adaptive resolution simulation (AdResS)
- [ ] Hybrid CG/AA methods
- [ ] CGMD → backmapping
- [ ] Mesoscale methods (DPD)
- [ ] Lattice Boltzmann methods
- [ ] Coupled continuum-atomistic

---

## 9. QM/MM Methods

### 9.1 QM/MM Frameworks

- [ ] Link atom scheme
- [ ] Frozen orbital boundary
- [ ] Pseudobond method
- [ ] Additive vs. subtractive QM/MM
- [ ] Mechanical embedding
- [ ] Electrostatic embedding
- [ ] Polarizable embedding
- [ ] QM/MM free energy perturbation
- [ ] ONIOM method
- [ ] QM/MM with NAMD (TcL-VMD interface)
- [ ] QM/MM in CP2K (GPW method)
- [ ] QM/MM in GROMACS (ORCA interface)

### 9.2 QM Methods Used in QM/MM

- [ ] Semi-empirical (AM1, PM3, PM6, PM7, GFN-xTB)
- [ ] DFT (B3LYP, PBE, ωB97X-D)
- [ ] SCC-DFTB
- [ ] HF reference
- [ ] MP2 in QM/MM
- [ ] CASSCF for excited states
- [ ] Time-dependent DFT (TD-DFT)

---

## 10. Analysis & Observables

### 10.1 Structural Analysis

- [ ] RMSD (root-mean-square deviation)
- [ ] RMSF (per-residue fluctuations)
- [ ] Radius of gyration (Rg)
- [ ] End-to-end distance
- [ ] Pair distribution function g(r)
- [ ] Radial distribution function
- [ ] Structure factor S(q)
- [ ] Solvent accessible surface area (SASA)
- [ ] Secondary structure assignment (DSSP, STRIDE)
- [ ] Contact maps & contact matrices
- [ ] Native contacts (Q)
- [ ] Hydrogen bond analysis
- [ ] Salt bridge analysis
- [ ] π-stacking
- [ ] Lipid order parameters (SCD)
- [ ] Membrane thickness & area per lipid
- [ ] Bilayer undulations

### 10.2 Dynamic Analysis

- [ ] Mean square displacement (MSD)
- [ ] Self-diffusion coefficient
- [ ] Velocity autocorrelation function (VACF)
- [ ] Orientational autocorrelation functions
- [ ] Rotational diffusion
- [ ] Principal component analysis (PCA / essential dynamics)
- [ ] Normal mode analysis (NMA)
- [ ] Quasi-harmonic analysis
- [ ] Dynamic cross-correlation matrix (DCCM)
- [ ] Time-lagged independent component analysis (tICA)
- [ ] TICA-based feature selection

### 10.3 Thermodynamic Properties

- [ ] Heat capacity
- [ ] Compressibility
- [ ] Bulk modulus
- [ ] Thermal expansion coefficient
- [ ] Dielectric constant
- [ ] Surface tension
- [ ] Viscosity (Green-Kubo)
- [ ] Thermal conductivity
- [ ] Self-diffusion via Einstein relation
- [ ] Osmotic coefficient

### 10.4 Spectroscopic Observables

- [ ] IR / Raman spectra from MD
- [ ] NMR order parameters (S²)
- [ ] Chemical shift prediction
- [ ] J-coupling prediction
- [ ] NOE-based validation
- [ ] SAXS/SANS profiles from MD
- [ ] Fluorescence anisotropy
- [ ] 2D-IR spectroscopy simulation

### 10.5 Energy Analysis

- [ ] Energy decomposition (bonded vs. non-bonded)
- [ ] Interaction energy between groups
- [ ] Per-residue energy decomposition
- [ ] MM-PBSA energy components
- [ ] Vibrational density of states (VDOS)
- [ ] Energy flow & vibrational energy transport

### 10.6 Markov State Models (MSM)

- [ ] Featurization for MSMs
- [ ] Dimensionality reduction (PCA, tICA)
- [ ] Clustering (k-means, mini-batch k-means)
- [ ] MSM lag time selection
- [ ] Chapman-Kolmogorov test
- [ ] Implied timescales
- [ ] Transition probability matrix
- [ ] Stationary distribution
- [ ] PCCA+ macrostate decomposition
- [ ] Committor functions
- [ ] MFPT from MSMs
- [ ] PyEMMA / deeptime
- [ ] MSMBuilder

---

## 11. System Preparation

### 11.1 Protein System Setup

- [ ] PDB structure acquisition & cleaning
- [ ] Missing residue / loop modeling
- [ ] Protonation state assignment (propKa, H++, Mcce2)
- [ ] Disulfide bond identification
- [ ] N- and C-terminal capping
- [ ] Histidine tautomer selection
- [ ] Protein in explicit solvent box
- [ ] Solvation box size & shape (cubic, dodecahedron, truncated octahedron)
- [ ] Ion placement (neutralization, concentration)
- [ ] Counterion placement (random vs. Debye-Hückel)

### 11.2 Membrane Systems

- [ ] CHARMM-GUI membrane builder
- [ ] PACKMOL-Memgen
- [ ] Bilayer lipid composition
- [ ] Mixed lipid bilayers (POPE/POPG/cholesterol)
- [ ] Membrane protein embedding
- [ ] Protein-lipid systems
- [ ] Membrane with asymmetric leaflets
- [ ] Detergent micelle systems

### 11.3 Ligand & Small Molecule Setup

- [ ] Ligand parameterization (GAFF, CGenFF)
- [ ] RESP charge derivation
- [ ] Ligand docking pose as starting structure
- [ ] Co-crystallized ligand preparation
- [ ] GCMC insertion of ligands
- [ ] Protein-ligand complex solvation

### 11.4 Minimization & Equilibration Protocols

- [ ] Steepest descent minimization
- [ ] Conjugate gradient minimization
- [ ] L-BFGS minimization
- [ ] Restrained equilibration (heavy atoms, backbone)
- [ ] Gradual pressure coupling ramp
- [ ] Temperature ramping
- [ ] NVT → NPT equilibration sequence
- [ ] Pre-production checks (density, energy drift)

---

## 12. MD Software & Implementation

### 12.1 GROMACS

- [ ] gmx pdb2gmx
- [ ] gmx grompp
- [ ] gmx mdrun
- [ ] gmx trjconv
- [ ] gmx energy
- [ ] gmx rms / rmsf
- [ ] gmx sasa
- [ ] gmx hbond
- [ ] gmx densmap
- [ ] mdp parameter file
- [ ] GROMACS topology (.top, .itp)
- [ ] .gro / .pdb coordinate files
- [ ] .tpr run input file
- [ ] .xtc / .trr trajectory formats
- [ ] GROMACS force field directory
- [ ] Free energy λ states in GROMACS
- [ ] PLUMED plugin integration
- [ ] GROMACS + GPU acceleration
- [ ] Domain decomposition
- [ ] PME grid settings in GROMACS
- [ ] GROMACS virtual sites

### 12.2 NAMD

- [ ] NAMD configuration file (.namd)
- [ ] namd2 / namd3 executables
- [ ] NAMD collective variables (colvars) module
- [ ] NAMD ABF / metadynamics via colvars
- [ ] NAMD FEP module
- [ ] Alchemical FEP in NAMD (.fep file)
- [ ] SMD in NAMD
- [ ] NAMD GPU acceleration
- [ ] NAMD scalability (petascale)
- [ ] NAMD periodic boundary setup
- [ ] NAMD ensemble MD
- [ ] NAMD REST2
- [ ] NAMD QM/MM (TcL scripting)

### 12.3 AMBER

- [ ] tleap / xleap for topology
- [ ] sander (CPU, serial MD)
- [ ] pmemd (GPU-accelerated MD)
- [ ] pmemd.cuda
- [ ] AMBER force field files (.prmtop, .inpcrd, .rst7)
- [ ] AMBER .mdcrd / .nc trajectory
- [ ] AMBER mdin input file
- [ ] AMBER REST2 / REMD
- [ ] AMBER free energy (FEP, TI)
- [ ] AmberTools suite
- [ ] cpptraj analysis
- [ ] MMPBSA.py
- [ ] Gaussian-accelerated MD (GaMD) in AMBER
- [ ] AMBER umbrella sampling

### 12.4 CHARMM

- [ ] CHARMM scripting language
- [ ] CHARMM PSF file
- [ ] CHARMM RTF / PRM parameter files
- [ ] CHARMM DCD trajectory
- [ ] CHARMM REMD
- [ ] CHARMM FEP / TI (PERT module)
- [ ] CHARMM membrane builder
- [ ] CHARMM normal mode analysis
- [ ] CHARMM MMFP (mean field)
- [ ] CHARMM-GUI workflows
- [ ] OpenMM backend from CHARMM

### 12.5 OpenMM

- [ ] OpenMM Python API
- [ ] OpenMM System & Topology objects
- [ ] CustomForce objects
- [ ] Integrator classes (Verlet, Langevin, BrownianIntegrator)
- [ ] OpenMM GPU acceleration
- [ ] OpenMM enhanced sampling (openmmtools)
- [ ] OpenMM MBAR/FEP
- [ ] Perses (automated FEP)
- [ ] OpenMM+PLUMED
- [ ] OpenMM forcefield XML files
- [ ] OpenMM serialization (XML state)
- [ ] openff-toolkit integration

### 12.6 LAMMPS

- [ ] LAMMPS input script
- [ ] LAMMPS data file format
- [ ] LAMMPS fix commands (NVT, NPT, NVE)
- [ ] LAMMPS pair_style
- [ ] LAMMPS bond/angle/dihedral styles
- [ ] LAMMPS REMD (temper command)
- [ ] LAMMPS FEP (compute fep)
- [ ] LAMMPS coarse-grained models
- [ ] LAMMPS GPU package
- [ ] LAMMPS KOKKOS package
- [ ] LAMMPS fix plumed
- [ ] LAMMPS mesoscale (DPD, SPH)
- [ ] LAMMPS polymer & materials workflows

### 12.7 Desmond

- [ ] Desmond trajectory format (.dms, .xtc)
- [ ] Maestro/Schrödinger GUI
- [ ] FEP+ workflow (RBFE/ABFE)
- [ ] Desmond barostats & thermostats
- [ ] Enhanced sampling in Desmond (REST2, metadynamics)
- [ ] WaterMap analysis
- [ ] Protein preparation wizard
- [ ] SiteMap
- [ ] Glide docking integration

### 12.8 CP2K

- [ ] CP2K input structure (sections & keywords)
- [ ] GPW (Gaussian and plane waves)
- [ ] GAPW method
- [ ] Born-Oppenheimer MD (BOMD)
- [ ] Car-Parrinello MD (CPMD)
- [ ] Metadynamics in CP2K (PLUMED)
- [ ] QM/MM in CP2K
- [ ] CP2K periodic DFT
- [ ] Kohn-Sham energies in CP2K

### 12.9 PLUMED (Plugin Ecosystem)

- [ ] PLUMED collective variables
- [ ] PLUMED metadynamics setup
- [ ] PLUMED well-tempered metadynamics
- [ ] PLUMED OPES
- [ ] PLUMED REMD/HREX
- [ ] PLUMED committor analysis
- [ ] PLUMED landmarks & path CVs
- [ ] PLUMED funnel metadynamics
- [ ] PLUMED DUMPFORCES / DUMP
- [ ] PLUMED replica averaging
- [ ] PLUMED with GROMACS / AMBER / NAMD / LAMMPS
- [ ] PLUMED NEST repository
- [ ] PLUMED sum_hills

### 12.10 Specialized & Emerging Codes

- [ ] Anton / Anton 2 (D.E. Shaw)
- [ ] Tinker / Tinker-HP (AMOEBA)
- [ ] DL_POLY
- [ ] OpenCL-based codes
- [ ] ACEMD (GPU-accelerated)
- [ ] Folding@home distributed MD
- [ ] HTMD (high-throughput MD)
- [ ] BioSimSpace
- [ ] MDAnalysis Python library
- [ ] MDTraj library
- [ ] pytraj / cpptraj Python interface
- [ ] parmed (parameter/topology manipulation)
- [ ] CHAP (channel annotation package)
- [ ] ProDy (ENM, PCA, NMA)
- [ ] WESTPA (weighted ensemble)

---

## 13. Machine Learning & AI-Driven MD

### 13.1 ML Force Fields (MLFF)

- [ ] Behler-Parrinello neural network potentials
- [ ] Deep potential molecular dynamics (DeePMD)
- [ ] NequIP (E(3)-equivariant NN)
- [ ] MACE
- [ ] SchNet
- [ ] DimeNet
- [ ] ANI-1 / ANI-2x
- [ ] PhysNet
- [ ] Gaussian approximation potentials (GAP)
- [ ] SOAP descriptors
- [ ] Moment tensor potentials (MTP)
- [ ] MLFF active learning strategies
- [ ] MLFF validation & uncertainty quantification

### 13.2 CV Discovery & Enhanced Sampling with ML

- [ ] TICA-based CVs
- [ ] Autoencoder CVs
- [ ] Variational approach to Markov processes (VAMPnets)
- [ ] Deep tICA
- [ ] Neural network MSMs
- [ ] RAVE (reweighted autoencoded variational Bayes)
- [ ] Deep-TICA
- [ ] Spectral gap optimization

### 13.3 Structure Prediction & MD

- [ ] AlphaFold2 structures as MD starting points
- [ ] ESMFold
- [ ] RoseTTAFold
- [ ] AF2 B-factor vs. MD RMSF comparison
- [ ] Intrinsically disordered protein (IDP) ensembles
- [ ] Structure refinement with MD

---

## 14. Special System Types

### 14.1 Membrane & Lipid Systems

- [ ] Lipid bilayer self-assembly
- [ ] Membrane protein MD (GPCR, ion channels)
- [ ] Lipid flip-flop
- [ ] Membrane curvature
- [ ] Raft formation in CG models
- [ ] Peripheral membrane protein binding
- [ ] Sterol dynamics
- [ ] Ganglioside patches

### 14.2 Nucleic Acids

- [ ] DNA duplex MD
- [ ] RNA folding simulations
- [ ] Protein-DNA interactions
- [ ] RNA-protein complexes
- [ ] Nucleosome MD
- [ ] Non-canonical DNA structures (G-quadruplex, i-motif)
- [ ] Force field choices for NA (BSC1, OL15, DESRES)

### 14.3 Intrinsically Disordered Proteins (IDPs)

- [ ] IDP force field comparisons
- [ ] Extended conformational sampling
- [ ] Transient secondary structure
- [ ] Ensemble validation (NMR, SAXS)
- [ ] IDP aggregation
- [ ] Fuzzy complexes

### 14.4 Materials & Solid State

- [ ] Crystalline solid MD
- [ ] Grain boundary simulations
- [ ] Defect migration
- [ ] Thermal conductivity in solids
- [ ] Polymer melt MD
- [ ] Polymer glass transition
- [ ] Metal nanoparticle MD
- [ ] Zeolite & porous material simulations
- [ ] MOF simulations
- [ ] Grand canonical Monte Carlo (GCMC) for gas adsorption
- [ ] Electrostatic tuning of porous carbon
- [ ] CO₂ capture simulations

### 14.5 Solvation & Interfaces

- [ ] Explicit vs. implicit solvation
- [ ] Ion solvation free energies
- [ ] Ionic liquids MD
- [ ] Protein-water interface
- [ ] Lipid-water interface
- [ ] Hydrophobic effect
- [ ] Water structure near surfaces
- [ ] Wettability simulations
- [ ] Electrochemical interfaces

---

## 15. Performance & HPC

### 15.1 Parallelization Strategies

- [ ] Domain decomposition (spatial)
- [ ] Force decomposition
- [ ] Atom decomposition
- [ ] OpenMP threading
- [ ] MPI parallelism
- [ ] GPU acceleration (CUDA, OpenCL, HIP)
- [ ] NVIDIA GPU MD (GROMACS, AMBER, NAMD)
- [ ] Mixed precision GPU MD
- [ ] KOKKOS portability layer
- [ ] SYCL / Intel GPU
- [ ] Hybrid CPU-GPU scheduling

### 15.2 HPC & Workflow Management

- [ ] SLURM job submission
- [ ] PBS/Torque job scheduling
- [ ] Checkpoint / restart protocols
- [ ] Automated pipeline tools (HTMD, BioSimSpace, MDAnalysis)
- [ ] Workflow managers (Snakemake, Nextflow, AiiDA)
- [ ] Ensemble MD (HTMD, WESTPA)
- [ ] Cloud-based MD (AWS, GCP, Azure)
- [ ] Folding@home architecture

### 15.3 Performance Benchmarks & Optimization

- [ ] PME grid optimization
- [ ] Neighbor list (Verlet buffer, link-cell)
- [ ] Non-bonded cutoff tuning
- [ ] Load balancing
- [ ] I/O optimization (HDF5, Zarr for trajectories)
- [ ] Trajectory compression
- [ ] Benchmarking GROMACS / AMBER / NAMD
- [ ] Memory bandwidth bottlenecks

---

## 16. Monte Carlo Methods

### 16.1 MC Sampling Schemes

- [ ] Metropolis-Hastings algorithm
- [ ] Grand canonical MC (GCMC)
- [ ] Gibbs ensemble MC
- [ ] Configurational bias MC (CBMC)
- [ ] Aggregation volume bias MC (AVBMC)
- [ ] Parallel tempering MC
- [ ] Expanded ensemble MC
- [ ] Wang-Landau sampling
- [ ] Flat-histogram methods
- [ ] MC in RASPA2
- [ ] MC in Cassandra
- [ ] MC in BOSS
- [ ] MC vs. MD for equilibrium sampling

---

## 17. Validation, Reproducibility & Best Practices

### 17.1 Simulation Validation

- [ ] Force field validation against experiment
- [ ] Convergence testing
- [ ] Block averaging & statistical error
- [ ] Autocorrelation time estimation
- [ ] Bootstrap / jackknife error analysis
- [ ] Comparing with NMR order parameters
- [ ] Comparing with SAXS / SANS
- [ ] Replica consistency checks
- [ ] Energy drift diagnostics
- [ ] Shadow Hamiltonian analysis

### 17.2 Reproducibility & Reporting

- [ ] Reporting force field version
- [ ] Sharing input files (Zenodo, MDDB, BioSimDB)
- [ ] ICoMSE recommendations
- [ ] CHARMM-GUI → reproducible inputs
- [ ] Software version pinning
- [ ] Trajectory archiving standards
- [ ] FAIR data principles for MD
- [ ] OSF / GitHub for MD protocols
- [ ] Reporting PME / barostat / thermostat settings

---

*~450 topics · Last updated: 2026-03*
