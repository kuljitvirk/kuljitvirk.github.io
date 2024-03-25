---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
---


I am a theoretical physicist applying my skills and insights from fundamental physics to technology development. I earned my PhD from the University of Toronto by applying the methods of quantum field theory to formulate a theory of non-linear optical response of semiconductor quantum wells at femto and pico-second timescales. 

I have spent 10 years with a diverse set of engineering teams designing complex hardware and software systems in 3 different companies in semiconductor industry. I will always be learning, but I have now acquired a deep understanding of the role of theory, simulation, and empirical data in reaching effective solutions to difficult engineering problems in optical imaging, detection of deep sub-wavelength anomalies in semiconductor devices, and the materials science in design of imaging systems at photon energies exceeding damage thresholds of most materials. The fundamental skillset in this area has many overlaps with nano-photonics, microscopy, sensing, and materials physics. 

In my current role at KLA, I lead a team investigating the fundamental limits of detecting 10 nm scale defects in CMOS circuitry using deep UV wavelengths (200 nm - 500 nm). This deep sub-diffraction detection is forced by the range of photon energies where most semiconductors, insulators, and metals interact strongly with light. Through our investigations, we propose solutions in the space of optical imaging modalities, statistical detection algorithms, and optimization of the composition of process monitoring wafers in semiconductor fabs around the world. 

My research at KLA builds on the significant advacements I made to efficiently compute the highly complex background formed by scattering from rough dielectric boundaries  against which the signals from real defects are to be detected. I built both the mathematical theory and the high performance computing infrastructure to enable large scale simulations of the sensitivity of optical inspection of current and future technology nodes. These simulations include a detailed modeling of the illumination, light matter scattering, and imaging in KLA's optical inspectors.

I also studied the probably approximately correct (PAC) learning framework and used it to design automated defect classifiers with false positive rates far beyond the state of the art at KLA.




I continue to pursue my deep curiosity and interest in theoretical condensed matter and optical physics on my own.  I like to test my understanding by writing up my own account of the topics, and implementing the key computations to slowly build up my capability to perform advanced calculations in many body physics and quantum optics. My notes on various topics can be accessed below and some of my codes in a share-able state are available at github: [pyMie](https://github.com/kuljitvirk/pyMie.git)  and [quantum](https://github.com/kuljitvirk/quantum.git).

In 2022, I started teaching myself the theory of quantum computing by working out problems in the book by Nielsen  & Chuang. I mastered the primitives such as quantum fourier transform, phase estimation, period finding and their applications to construct Shor and Grover algorithms. I then learned error correcting codes, toric codes, and have recently started to investigate the application to qubit systems to solve problems in quantum chemistry. My goal of this study is to understand by working out myself what problems are accessible with the present capabilities of qubit devices. In the process, I am hoping to gain expertise on the clever approximations and the key libraries such as Cirq and Qiskit to formulate solutions in terms of quantum circuits.

### Notes:

* [Techniques in analysis of chaotic random networks and spin glasses](src/SpinGlassTechniques.pdf).
* [Technical Notes on Quantum Computing](src/QuantumComputing01.pdf).
* [Error correcting codes and stabilizers](src/QuantumComputing02.pdf).
* A general [derivation of Lindblad master equations](src/MasterEquations.pdf) to second order in system-bath coupling.
* [Fresnel reflection at Uni-axial interfaces](src/Fresnel.pdf)
* [Mie theory](src/mie_theory.pdf) with detailed near and far field expressions. Implementation validated against various sources in the literature can by found at [pyMie](https://github.com/kuljitvirk/pyMie.git).
