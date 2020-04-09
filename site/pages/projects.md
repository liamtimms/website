---
title: Research Projects
---

Over the course of my PhD, I have worked primarily on magnetic resonance imaging (MRI) research.

## QUTE-CE MRI
Quantitative Ultrashort-Time-to-Echo Magnetic Resonance Imaging (QUTE-CE MRI) is a technique initially developed in Prof. Sridhar's lab by a number of collaborators particularly Codi Gharagouzloo, Saausan Madi and Praveen Kulkani. The essence of the technique is the optimization of Ultrashort-Time-to-Echo (**UTE**) sequences for imaging T1 shortening contrast agents with long circulation times. The most powerful of such agents available are super-paramagnetic iron oxide nanoparticles (SPIONs) and we have optimized the technique with a specific focus on the commercially available FDA approved iron supplement **Ferumoxytol**. The combination of UTE sequences with Ferumoxytol maximizes positive T1 weighted contrast while minimizing multiple common artifacts associated with traditional contrast enhanced MRI.
In a paper I co-first authored with Dr. Gharagouzloo, we demonstrated the technique can be used to image blood vessels and blood volume in the rat brain \cite{Gharagouzloo2017}. I am currently responsible for much of this ongoing project as it is the subject of my in-progress PhD thesis:

* In 2017 we started a clinical trial for QUTE-CE MRI for the first time in human subjects. In this **clinical trial** of the technique for brain imaging, I...
    + designed and implemented the scan protocol and pulse sequences using Seimen's WIP 992 collaboratively with vitally important collaborators
    + interfaced with the volunteer research subjects (after their recruitment) to set them up in the scanner
    + operated the Seimens' 3T PRISMA MRI scanner
    + fully developed a custom analysis pipeline written in python using nipype, FSL, Freesurfer, SPM, ANTs, and some of my additional custom scripts (MATLAB and python) to analyze the resulting data
    + completed the majority of the data analysis using said pipeline
    + wrote the majority of the text for the pending publications of this work

* I also work on development of the technique for **functional imaging**:
    + My initial interest in the technique was for it's potential use for measurement of blood volume across the brain
    + In the 2017 paper we demonstrated that changes in blood volume could be measured between long lasting brain states (eg. awake vs anesthetized)
    + I have worked on expanding the technique to faster scans for imaging of the blood volume changes in different brain regions as a result of functional activity

* Application of the technique to animal models of **drug addiction**:
    + my first grant as a PI (albeit on a dissertation proposal)
    + I focus on using my current developments on improving, expanding and optimizing the technique to study animal models of drug addiction
    + for these pre-clinical scans I use a 7T Bruker scanner in the Center for Translational NeuroImaging (CTNI) at Northeastern University
    + this is the first application of function imaging with the technique to
    + additionally it involves combination of the technique with other pulse sequences which can use Ferumoxytol as a contrast agent

## MRArch
As part of the above QUTE-CE MRI project, I had to use a number of neuroimaging tools together, many of which are bing actively improved and updated by the outstanding open-source neuroscientific/medical imaging communities. I wanted a way to automatically set-up and use the state of the art versions of these imaging suites together in concert. Nipype solves the problem of how to integrate multiple tools together and the features of Arch Linux allow easy scripting of software installation and updates for the community. Thus, out of necessity I created a basic script for installing and configuring all major neuroimaging software on Arch Linux (mainly using the community run Arch User Repository) and contributed to or created multiple packages on that repository: <https://aur.archlinux.org/packages/?O=0&SeB=M&K=liamtimms&outdated=&SB=n&SO=a&PP=50&do_Search=Go>


