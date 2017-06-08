---
layout: page
title: CBB752 Spring 2017
tagline: Final Project
---

Project Title
------------------
CRISPR and personal genomics: The impact of SNPs on sgRNA sets and off target mutations

Table of Contents
-----------------------




**Contributors**
 -Writing:
 -Coding: Jiawei Wang
 -Pipeline:

### Introduction:





### Writing:








### Coding:
Propose a tool that finds PAM sites in the human reference genome as well as Carl’s genome and compares the similarity of the two sets.
Here final2-2.a.py is the integrated version, and final2-2.2.1.py and final2-2.2.2.py are functionally separate versions.

#### Documentation:
##### final2-2.2.1.py
Version 2.1. Previous versions import the exported Spyder data format zids.spydata to include Zimmerome SNP information (to save time). Here it uses .pickle format data to allow automatic read-in.

##### final2-2.2.2.py
Version 2.2. This version generates a statistic sheet of number, and changed number and rate due to SNPs of two genomes.

##### final2-2.a.py
Version 4/a. This file basically integrates all the previous code together.

##### Usage
The most useful version is version 2.1, 2.2.

Command line example of final2-2.2.1.py:
> python final2-2.2.1.py -i <input folder> -m <mutation file> ###USAGE

> python final2-2.2.1.py -i Genome_GRCh37 -m Z.variantCall.SNP_filt.vcf #or zids.pickle if generated ###EXAMPLE

> ###generate mutation site figures and changed sites.

##### Requirement
Here I use Python 2.7. 
Files needed include Zimmerome SNP file (Z.variantCall.SNPs.vcf, from https://zimmerome.gersteinlab.org/2016/05/06/part01_gerstein/, but its comment was removed to generate a readable table), 
reference genome sequence (here I use GRCh37 downloaded from UCSC Genome Browser).

#### Results:
Results include 3 parts:
  1. Sample PAM sites distribution (plot out first 100 PAM sites of the two genomes against chromosome position): SamplePlot_chr*.png
  2. Histogram of PAM sites distribution on different parts of genomes, 100 bins: Histogram_chr*.png
  3. Scatterplot of PAM sites distribution on differetn parts of genomes, 10000 points: ScatterHist_chr*.png
  4. List of gained and lost PAM sites due to Zimmerome SNPs by each chromosome: Difference_*.txt
  5. Summary results of the effect of Zimmerome SNPs, including number of #PAM sites, #gained, %gained, #lost and %lost: ZSNPs_stats.txt

They are all in folder ./coding_results. It shows that PAM sites have an uneven distribution on each chromosome, which may reflect chromosomal structure and transcription activity. It also shows that the Zimmerome SNPs have a 0.2% to 0.3% change of PAM sites on each chromosome (both gained and lost sites, except chromsome Y). So if large scale CRISPR experiments are not carried out at the same time, the influence (chance of off-target due to SNPs) should be very low. But the lists of changed PAM sites due to SNPs are generated and stored as well for reference during sgRNA design to avoid possible off-target due to SNPs.


### Pipeline:


#### Documentation:


#### Results:









#### Conclusions:








#### References:

 References can be included here or at the end of each relevant section.
 
 
