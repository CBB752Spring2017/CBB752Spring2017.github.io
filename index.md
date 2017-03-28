---
layout: page
title: CBB752 Spring 2017
tagline: Final Project
---

About the Course
------------------
- **Title:** Biomedical Data Science: Mining and Modeling
- **Instructor:** [Mark Gerstein](<http://www.gersteinlab.org>)
- **TAs:** Mengting Gu, Paul Muir
- **Introduction:** Bioinformatics encompasses the analysis of gene sequences,
    macromolecular structures, and functional genomics data on a large scale. It
    represents a major practical application for modern techniques in data
    mining and simulation. Specific topics to be covered include sequence
    alignment, large-scale processing, next-generation sequencing data,
    comparative genomics, phylogenetics, biological database design, geometric
    analysis of protein structure, molecular-dynamics simulation, biological
    networks, normalization of microarray data, mining of functional genomics
    data sets, and machine-learning approaches to data integration.
- **More Information:** Check out the [course website](<http://cbb752b17.gersteinlab.org>).

Final Project
-----------------------

**Due: May 9th 11:59PM**

Students will form teams to work on one of the following topics of interest, though we are open to other potential projects if they are clearly articulated and of comparable scope to these listed below. The submitted final projects will be published on this website. It will also serve as a reference for later students and researchers.

### Topics

#### Part 1: Comparative analysis of personal genomes:

**-1. Compare the variants in Carl’s genome with those in the gnomAD and 1000 Genomes databases. Compare and contrast the results from the two databases.**

**Writing:** Describe the 1000 Genomes and gnomAD databases and what can be learned from collections of variants observed in large populations. How have these databases evolved over the past decade?

**Coding:** Propose a tool that finds information on a subset of Carl’s variants in the gnomAD and 1000 genomes databases.

**Pipeline:** Identify and run a tool that finds the population frequencies for each of the variants observed in Carl’s genome and also look to see how many are private variants. How do these number change based on the two databases used?


**-2. Compare the variants in Carl’s genome with those found in the GTEx database. Use the results to predict gene expression in various tissues and better estimate the impact of noncoding variants in Carl’s genome.**

**Writing:** Describe eQTLs and the GTEx database. How was the data present in GTEx generated and what scientific questions does it help answer?

**Coding:** Propose a tool to identify eQTLs in a subset of Carl’s variants using the GTEx database. What expression changes would you predict in Carl? Make sure to cover tissues that can be easily assayed.

**Pipeline:** Process the variants in Carl’s genome to identify any eQTLs. Look at multiple tissues (make sure to include tissues that might be able to be tested in a noninvasive manner e.g. blood).


**-3. Analyze at the protein coding mutations in the Zimmerome**

**Writing:** Explain the different types of functional information that can be incorporated into a variant prioritization scheme. Describe both the features that were chosen as well as those not included but which might be useful to incorporate in the future.

**Coding:** Propose a tool to rank the deleteriousness of the identified protein coding mutations in Carl’s genome. In the case of nonsynonymous mutations look at different properties of the new amino acid relative to the original. This might include size, charge, etc. For synonymous mutations look at the codon preferences in humans. For stop codon introduction or removal look at the change in length of the new protein relative to the original.

**Pipeline:** Look at various functional prediction programs and process Carl’s variants in the provided VCF file. How much agreement is observed between the different scores?


#### Part 2: Personal genomes and personalized medicine (CRISPR):

**-1. Identifying off target CRISPR sites**

**Writing:** Explain the risk of off target mutations due to CRISPR. What factors determine the likelihood of a CRISPR guide RNA cutting at an off target site? 

**Coding:** Propose a tool that identifies off target CRISPR sites given a genome and guide RNA sequence.

**Pipeline:** Using two off target site prediction programs look at the predicted off target sites and compare to empirical observations in this [paper](<https://genomebiology.biomedcentral.com/articles/10.1186/s13059-016-1012-2>).


**-2. CRISPR and personal genomics: The impact of SNPs on sgRNA sets and off target mutations.** 

**Writing:** How might SNPs in Carl's genome impact the use of CRISPR as a treatment? Read this [paper](<http://palgrave.nature.com/nbt/journal/v34/n2/full/nbt.3437.html>) about the design of guide RNAs. Discuss how individual SNPs would impact the off-target effects in the presence of the SNP. 

**Coding:** Propose a tool that finds PAM sites in the human reference genome as well as Carl’s genome and compares the similarity of the two sets.

**Pipeline:** Calculate the sgRNA libraries for the reference genome and Carl's genome. How different are these two sets? See this [paper](<http://www.nature.com/nbt/journal/vaop/ncurrent/full/nbt.3804.html?WT.feed_name=subjects_genetics>).


**-3 Analysis of CRISPR-targeted deaminases. See this [paper](< http://www.nature.com/nature/journal/v533/n7603/abs/nature17946.html>) for background.**

**Writing:** What benefits do CRISPR-targeted deaminases have over CRISPR approaches that rely on double stranded breaks? What are the drawbacks?

**Coding:** Propose a tool that creates sgRNAs for CRISPR-targeted deaminases. How many of Carl's SNPs could be changed? How many nonsynonymous protein coding changes in Carl's genome could be reverted?

**Pipeline:** How many disease associated SNPs could CRISPR-targeted deaminases edit?


#### Part 3: Network analysis of personal genomes:

**-1. Propose a tool that calculates the degree centrality and betweenness centrality of proteins containing and not containing SNPs in Carl’s genome using a PPI file. PPI data can be downloaded from DIP, BIND, MIPS, MINT, and InAct databases.**


#### Part 4: Structure Analysis

**-1. Similar to Assignment 3, but look at structure of mutant type of 3VKO. Look at mutations at location 19: F19Y, F19I, F19L, and compare to the wild type. Perform side chain rotations for these mutant residue at location 19 and calculate the lowest energy conformation for each.**

**-2. Similar to Assignment 3, but look at structure of mutant type of 3VKO. Look at mutations at location 35: I35L, I35F, I35V, and compare to the wild type. Perform side chain rotations for these mutant residue at location 35 and calculate the lowest energy conformation for each.**
