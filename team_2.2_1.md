---
layout: page
title: Final project 2.2
tagline: Final Project
---

Project Title
------------------
CRISPR and personal genomics: The impact of SNPs on sgRNA sets and off target mutations

Table of Contents
-----------------------

### Writing:

Cas9 activity depends on both sgRNA sequence and experimental conditions. While obviously conditions inside the human body are difficult to control, knowledge of sgRNA sequence will greatly impact the effect of CRISPR/Cas9 efficiency. The many SNPs in Carl’s genome may lead to a variety of different off-target effects, mostly negative, which can be alleviated via well thought out application of CRISPR guide RNA selection rules, such as Rule Set 1 and Rule Set 2 as referenced in Doench et. al., as well as well established predictive algorithms to find off-target effects in silico.
Overall, stochastic introduction of SNPs will generate novel NGG sites relative to any guide genome, leading to poor effects from any “generalized” CRISPR therapeutic strategies. Obviously, any CRISPR therapeutics will therefore require an initial genome sequencing to ensure that a full knowledge of potential S. pyogenes CRISPR sites is known. Additionally, any SNPs in guide sequence areas would lead to lower Cas9 cleavage rates at those loci. Base-pair mismatches will lead to decreased affinity in on-target sites, but may also lead to increased affinity in off-target sites. Using techniques such as tru-gRNA (truncated guide RNA) or a gRNA extension could also lead to more specific cleavage, but this again would be affected by SNP changes. Overall, the best way to avoid SNPs causing both undesired off-target effects or decreased therapeutic efficiency is probably through thorough sequencing and screening of the patient-genome prior to construction of CRISPR gRNA sequences.


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

They are all in folder [./coding_results](https://github.com/CBB752Spring2017/final-project-2-2-team1-team-2-2-1/tree/master/coding_results). It shows that PAM sites have an uneven distribution on each chromosome, which may reflect chromosomal structure and transcription activity. It also shows that the Zimmerome SNPs have a 0.2% to 0.3% change of PAM sites on each chromosome (both gained and lost sites, except chromsome Y). So if large scale CRISPR experiments are not carried out at the same time, the influence (chance of off-target due to SNPs) should be very low. But the lists of changed PAM sites due to SNPs are generated and stored as well for reference during sgRNA design to avoid possible off-target due to SNPs.


### Pipeline:


#### Documentation:


#### Results:









#### Conclusions:

### [Source code](https://github.com/CBB752Spring2017/final-project-2-2-team1-team-2-2-1)
### [Slides](https://github.com/CBB752Spring2017/final-project-2-2-team1-team-2-2-1/blob/master/presentation_2.2.pptx?raw=true)

#### References:

 References can be included here or at the end of each relevant section.
 
 
