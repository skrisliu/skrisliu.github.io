---
layout: post
title: "sMRI Brain Image Preprocessing"
author: "skrisliu"
categories: technote
tags: [technote]
---

This post records how I preprocessed MRI brain images.

### Key
- Key paper: Brain Age Estimation From MRI Using Cascade Networks With Ranking Loss. Trans on Medical Imaging.
- Software: FSL which is only run on Linux, not Windows!!! They used FSL 5.10. I am using FSL 6.00
- Open Datasets: ADNI (N=1020), OASIS (3 phases, N=2926), PAC-2019 (N=2640, cannot download)

### Steps
Preprocessing includes nonlinear registration to the standard MNI space, brain extraction, voxel value normalization (subtracting the mean and dividing the standard deviation of voxel values within the brain area). All images after processed are with voxel size of 91$$\times$$109$$\times$$91 with isotropic spatial resolution of 2 mm$$^3$$. 

Needs to add the "fsl_anat_tsan" from their repo to the FSL directory, which is located slightly different with FSL 5.10 on the FSL 6.00 version. 
