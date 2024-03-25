---
layout : page
title : Selected R&D accomplishments
permalink: /rd
---


### Efficient modeling of optical scattering in complex networks of nano-structures


Link to publication on [Optica](https://opg.optica.org/josab/abstract.cfm?uri=josab-38-6-1763), and [arXiv](https://arxiv.org/abs/2105.03366).

**Introduction:** Scattering of light by isolated defects arises in many areas of nano-photonics and microscopy. A large-scale industry application is the inspection of nanometer-scale CMOS circuitry on patterned semiconductor wafers. Design of such inspection systems, and their optimal use require extensive modeling to map out the sensitivity of detection over the available wavelengths, imaging modalities, and sometimes the tunable layer thicknesses of the wafer itself. This modeling involves solving light-matter interaction in high dielectric structures numerically exactly, followed by computing the far field imaging of the scattered light. Present approaches to compute th scattering by deeply sub-wavelength isolated defects in these backgrounds rely on either the Born approximation and its quasi-analytic extensions or ab initio computation that requires large domain sizes to reduce the effects of boundary conditions. The Born approximation and its extensions are limited in scope, while the ab initio approach suffers from its high numerical cost. 

**My Contribution:** I invented a numerical method in which an effective local electric susceptibility tensor of a defect in an arbitrarily complex background is estimated by solving an inverse problem efficiently. The estimated tensor is embedded into an S-matrix formula based on the reciprocity theorem. With this embedding, the computation of the S-matrix of the defect requires field solutions only in the unit cell of the background. In practice, this scheme reduces the computational cost by almost two orders of magnitude, while sacrificing little in accuracy. The scheme demonstrates that statistical estimation can capture sufficient information from cheap calculations to compute quantities in the far field.

A special case of this technique is a highly effective solution to model the scattering of light by roughness at dielectric boundaries, ie. line edge roughness, variation of critical dimensions, and surface roughness. These problems can be treated with unperturbed fields but using an anisotropic susceptibility tensor that follows from Maxwell Garnett theory. That this is the correct tensor was proved by S. Johnson by taking the limit of the perturbation expansion of a smooth interface to an abrupt one. I applied this tensor to build a highly accurate solution to compute *ab-initio* the contribution of scattering by roughness to the signal-to-noise ratio. Compared to conventional methods based on super-cells, this technique is nearly 10,000 times faster to simulate a modern interconnect back end layer with a pitch of 20 nm.

I carried out highly successful program at KLA by applying these methods to scope out potential imaging solutions, optical design of future inspection systems, and with major chipmakers to optimize the composition of specialized wafers designed for monitoring defect formation in semiconductor manufacturing. 


### High accuracy machine learning for defect classification

A critical step in process monitoring in semiconductor device manufacturing is the classification of abnormalities of the printed circuit topology into *device disabling* defects and non-defects. These classifications are performed on electron microscope images of nanometer scale features in these circuits. At high yield, only a few defects may be expected among hundreds of thousands to millions of images. This requires a false positive rate several orders of magnitude below the state of the art. I built such automated classifiers by combining classical weak learning theory and neural networks to reach the accuracy needed. My patent submitted by KLA is currently pending. 

### Design and implementation of quantum and optoelectronic device simulators

For about 3 years, I built simulators for semiconductor quantum well lasers, light emitting diodes, quantum well photodetectors, and electro-optic modulators. I designed and implemented modules for meshing of the device, in-line computation of the optical response as a function of bias, the rate equations for carrier and photon density, and integrated them with direct and iterative solvers. 

In my most complex semiconductor laser simulation, I implemented an 8-band k.p model for a multiple quantum well active region including the coupling to the d.c. electric field of the external bias. The model employed 1D finite element model to solve for the electronic structure as a function of the device bias and the resulting change in the dielectric function of the active region as well as sponataneous emission rate from the conduction-to-valence state transitions. The entire problem was solved self-consistently with the laser cavity modes to compute the charge and photon density in the device. At that time, the model was offered through the Atlas device simulator by Silvaco. 





### Many Body Physics of Photo-Excited Solids

I applied the methods of quantum field theory, and in particular non-equilibrium Green's functions, to formulate a theory of decoherence in optically excited semiconductors. This was part of my PhD research with John Sipe in the Dept. of Physics at the University of Toronto. It represented an early attempt to derive non-linear optical susceptibility of many body systems beyond those with Hartree-Fock ground states. 

The key insight in this work was to formulate the order-by-order expansion of the correlation functions starting from a *quasi-equilibrium* state rather than the Hartree-Fock state. I derived the dynamical equations for the multi-electron Green functions, and showed how they can be reduced to the master equation of the Lindblad form under assumptions of low density. This work also revealed an immense complexity in the non-linear susceptibility expansion that results from the correlations in the ground state, which are absent in Hartree-Fock theory. My work culminated in publication of two long articles, [Phys. Rev. B 80, 165318](https://journals.aps.org/prb/abstract/10.1103/PhysRevB.80.165318), and [Physical Review B, 80, 165319](https://journals.aps.org/prb/abstract/10.1103/PhysRevB.80.165319). 

The technological advancements in ultrafast laser spectroscopy to observe the phenomena that my theory describes has become possible only 8-10 years after this publication. I did not push this work any further, having left academia shortly after. It lay dormant for most of the years with occassional interest from the many body physics researchers. I have also learned a great deal since then about high performance computing, and much has advanced in computational technology to more accurately predict the optical response of materials. I plan to revisit this work and pick up where I left. 

### Toplogical physics in electron dynamics

I invented a method to optically excite semiconductor quantum wells into a state with a transient Berry curvature at macroscopic scale. The theoretical study of this technique for a GaAs quantum well was published in [Phys. Rev. Lett. 107, 120403 (2011)](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.107.120403). I showed how to probe this transient non-trivial Berry curvature by a terahertz pulse. The effect was later used by experimentalists to delineate intrinsic and extrinsic spin hall effects -- a long-standing problem of considerable interest in spintronics.

My second contribution is computational. I invented a numerical technique  for using the length gauge to model the coherent motion of electrons driven by electromagnetic fields [[Phys. Rev. B 76, 035213](https://journals.aps.org/prb/abstract/10.1103/PhysRevB.76.035213)]. The length gauge is free of the impact of the unphysical divergences of the textbook form for coupling charges to the electromagnetic fields -- the velocity gauge. 

The key impediment to using the length gauge in computation is that the the electric field must couple to a gauge field in the momentum space, called the *Berry connection*. The Berry connections is the fundamental quantity for describing polarizability and the physics of topological insulators. 

The technique I contributed, required no *explicit* calculation of the Berry connection, but accounted for its physical effects *exactly*. My insight was to borrow the idea of *Wilson loop* in lattice gauge theory and formulate the transition of electron from one momentum state to another over a single time step with a *link* -- a matrix for transforming from one set of Bloch states to those at a shift in the crystal momentum. The shift arises from the acceleration by the external field over a single time step. The same idea in real space describes parallel transport in any curved space-time. 

This approach removed completely the effects of unphysical divergeneces in the velocity gauge that result from its breaking of the mass-sum rule in any practical calculation with a finite set of energy states. It simultaneously retains the full effects of the band topology . This technique is regularly cited in modeling of terahertz excitations of semiconductor quantum wells, and the key idea has been used by many researchers around the world. 

### Quantum kinetics of charge and energy transer

As a postodc at Columbia, I derived an effective microscopic theory for charge and energy transfer between quantum dots and electrodes, [see Phys. Rev. B 87, 205426](https://journals.aps.org/prb/abstract/10.1103/PhysRevB.87.205426). In it, I introduced a master equation for electronic degrees of freedom and derived all its couplings from the underlying micrscopic Hamiltonian and showed, through a detailed application, how to compute them from electronic structure calculations (specifically the density functional theory). The quantum dynamics formulated in this method accounted for the Fermi edge singularities in the ground state of the electrode through a transformation similar to the polaron transform in condensed matter physics. The computations demonstrated how the edge singularities can impact charge transfer rates. I also showed how the plasmonic excitations can non-radiatively cool quantum dots near metal surfaces. During this work, I also learned to use density functional theory for modeling metal surfaces. This work was done in collaboration with Mark Hybertsen (then at Brookhaven) and David Reichman (Dept. of Chemistry at Columbia).


