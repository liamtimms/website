---
title: Research Projects
---

Over the course of my PhD, I have worked primarily on magnetic resonance imaging (MRI) research.

## QUTE-CE MRI

Quantitative **Ultrashort-Time-to-Echo** Magnetic Resonance Imaging (QUTE-CE MRI) is a technique initially developed in Prof. Sridhar's lab by a number of collaborators; particularly Codi Gharagouzloo with Saausan Madi and Praveen Kulkani. The essence of the technique is the optimization of Ultrashort-Time-to-Echo (**UTE**) sequences for imaging T1-shortening contrast agents. The most powerful of such agents available are super-paramagnetic iron oxide nanoparticles (SPIONs) and we've been using the technique with a specific focus on the commercially available FDA approved iron supplement **Ferumoxytol**. The combination of UTE sequences with Ferumoxytol maximizes positive T1-weighted contrast while minimizing a few common artifacts associated with traditional contrast-enhanced MRI.

### Preclinical Work

In a paper I co-first authored with Dr. Gharagouzloo, we demonstrated the technique can be used to image blood vessels and blood volume in the rat brain \cite{Gharagouzloo2017}.

- I also work on development of the technique for **functional imaging**:

  - My initial interest in the technique was for its potential use in measurement of dynamic blood volume changes across the brain
  - In the 2017 Neuroimage paper, we demonstrated that changes in blood volume could be measured between stable brain states (eg. awake vs anesthetized)
  - I have worked on expanding the technique to faster scans for imaging of the blood volume changes in different brain regions as a result of functional activity

- Application of the technique to animal models of **drug addiction**:
  - my first grant as a PI (albeit on a dissertation proposal)
  - I focus on using my current developments on improving, expanding and optimizing the technique to study animal models of drug addiction
  - for these pre-clinical scans I use a 7T Bruker scanner in the Center for Translational NeuroImaging (CTNI) at Northeastern University
  - this is the first official application of the tecnqiue for imaging of active functionl changes
  - additionally, it involves combination of the technique with other pulse sequences which can use Ferumoxytol as a contrast agent

### Clinical Work

I am currently responsible for much of this ongoing project as it is the subject of my in-progress PhD thesis:

- In 2017 we started a clinical trial for QUTE-CE MRI for the first time in human subjects. In this **clinical trial** of the technique for brain imaging, I...
  - worked on the implementation of the scan protocol using a Siemens WIP with vitally important collaborators
  - lead the organization of the project on both the scanning logistics and the data analysis
  - interfaced with the volunteer research subjects (after their recruitment) to set them up in the scanner
  - operated the Seimens 3T PRISMA MRI scanner
  - fully developed a custom analysis pipeline written in python using nipype, FSL, Freesurfer, SPM, ANTs, and some of additional custom scripts (MATLAB and python) to analyze the resulting data
  - completed the majority of the data analysis using said pipeline
  - wrote the majority of the text for the pending publications of this work
- In 2020, we began moving forward with additional clinical projects. Publications pending!

## MRArch

As part of the above QUTE-CE MRI project, I had to use a number of neuroimaging tools together. Since this is an area of active research and continous development, many of these tools are constantly improved and updated by the outstanding open-source neuroscientific/medical imaging communities. I wanted a way to **automatically set-up and use the state of the art neuroimaging suites** together in concert, as simply as possible.

### The AUR

The Arch User Repository (AUR) is a site provided by the Arch Linux project which contains download, build and install recipes to package software for installation and use with the system *pac*kage *man*ager (pacman). This allows software to be distributed through 3rd party sites but installed and updated through native system tools. Out of necessity I created a basic script for installing and configuring all major neuroimaging software on Arch Linux (mainly using the community run Arch User Repository) and I have contributed to or created multiple packages on that repository: <https://aur.archlinux.org/packages/?O=0&SeB=M&K=liamtimms&outdated=&SB=n&SO=a&PP=50&do_Search=Go>

I've currently labeled this side-project (the combination of the install scripts and community packages) - Magnetic Resonance Analysis on Arch Linux (`MRArch`). While `Nipype` provides easy integration of multiple neuroimaging applications into powerful workflows, MRArch allows easy installation, automatic updates and simple management of these applications on one platform.

### The Script and Instructions

See here for the main page:

See here for the documentation:

### Comparison to Similar Projects

Using Arch Linux as a base provides bleeding edge features at the cost of stability/reliability. Users need to take into account the benefits and risks for this model. These other two projects also aim to provide various neuroimaging software programs together and should be examined before choosing one:

- [Neurodocker](https://github.com/ReproNim/neurodocker) - many of these same programs in docker containers
- [Neurodebian](https://neuro.debian.net/) - many of these same programs packaged for Debian and Ubuntu
