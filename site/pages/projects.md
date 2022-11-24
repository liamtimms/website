---
title: Research Projects
---

For my Ph.D., I worked primarily on magnetic resonance imaging (MRI) research.

## QUTE-CE MRI

Quantitative **Ultrashort-Time-to-Echo** Magnetic Resonance Imaging (QUTE-CE MRI) is a technique initially developed in Prof. Sridhar's lab by several collaborators, particularly Codi Gharagouzloo with Saausan Madi and Praveen Kulkani. The essence of the method is the optimization of Ultrashort-Time-to-Echo (**UTE**) sequences for imaging T1-shortening contrast agents. Super-paramagnetic iron oxide nanoparticles (SPIONs) are the most potent agents available. We've been using the technique mainly focusing on the commercially available FDA-approved iron supplement **Ferumoxytol**. Combining UTE sequences with Ferumoxytol maximizes positive T1-weighted contrast while minimizing a few common artifacts associated with traditional contrast-enhanced MRI.

### Preclinical Work

In a paper I co-first authored with Dr. Gharagouzloo, we demonstrated the technique could be used to image blood vessels and blood volume in the rat brain \cite{Gharagouzloo2017}.

- I also work on the development of the technique for **functional imaging**:

  - My initial interest in the technique was for its potential use in the measurement of dynamic blood volume changes across the brain
  - In the 2017 Neuroimage paper, we demonstrated that the technique could measure changes in blood volume between stable brain states (e.g., awake vs. anesthetized)
  - I have worked on expanding the technique to faster scans for imaging the blood volume changes in different brain regions as a result of functional activity

- Application of the technique to animal models of **drug addiction**:
  - my first grant as a PI (albeit on a dissertation proposal)
  - I focus on using my current developments to improve, expand, and optimize the technique to study animal models of drug addiction
  - for these preclinical scans, I use a 7T Bruker scanner in the Center for Translational NeuroImaging (CTNI) at Northeastern University
  - this is the first official application of the technique for imaging active functional changes
  - additionally, it involves the combination of the technique with other pulse sequences, which can use Ferumoxytol as a contrast agent

### Clinical Work

- In 2017, we started a clinical trial for QUTE-CE MRI for the first time in human subjects. In this **clinical trial** of the technique for brain imaging, I...
  - worked on the implementation of the scan protocol using a Siemens WIP with vitally important collaborators
  - lead the organization of the project on both the scanning logistics and the data analysis
  - interfaced with the volunteer research subjects (after their recruitment) to set them up in the scanner
  - operated the Seimens 3T PRISMA MRI scanner
  - fully developed a custom analysis pipeline written in python using nipype, FSL, Freesurfer, SPM, ANTs, and some additional custom scripts (MATLAB and python) to analyze the resulting data
  - completed the majority of the data analysis using said pipeline
  - wrote the majority of the text for the pending publications of this work
- In 2020, we began moving forward with additional clinical projects. Publications are pending!

## MRArch

As part of the above QUTE-CE MRI project, I used many neuroimaging tools together. However, since this is active research and continuous development, many of these tools are constantly improved and updated by the outstanding open-source neuroscientific/medical imaging communities. Therefore, I wanted a way to **automatically set up and use the state-of-the-art neuroimaging suites** together in concert, as simply as possible.

### The AUR

The Arch User Repository (AUR) is a site provided by the Arch Linux project which contains download, build and install recipes to package software for installation and use with the system **pac**kage **man**ager (pacman). This allows any piece of software to be distributed through 3rd party sites but installed and updated through native system tools. Out of necessity, I created a basic script for installing and configuring all major neuroimaging software on Arch Linux (mainly using the community-run Arch User Repository). I have contributed to or created multiple packages on that repository: <https://aur.archlinux.org/packages/?O=0&SeB=M&K=liamtimms&outdated=&SB=n&SO=a&PP=50&do_Search=Go>.

I've labeled this side-project (the combination of the install scripts and community packages) - Magnetic Resonance Analysis on Arch Linux (`MRArch`). While `Nipype` provides easy integration of multiple neuroimaging applications into powerful workflows, MRArch allows easy installation, automatic updates, and simple management of these applications on one platform.

### The Script and Instructions

See here for the main page:

TODO

See here for the documentation:

TODO

### Comparison to Similar Projects

Using Arch Linux as a base provides bleeding-edge features at the cost of stability/reliability. Users need to take into account the benefits and risks of this model. These other two projects also aim to provide various neuroimaging software programs together and should be examined before choosing one:

- [Neurodocker](https://github.com/ReproNim/neurodocker) - many of these same programs in docker containers
- [Neurodebian](https://neuro.debian.net/) - many of these same programs packaged for Debian and Ubuntu

#
