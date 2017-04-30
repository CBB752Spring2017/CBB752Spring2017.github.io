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

The end product of the final project will consist of a GitHub page detailing the work of each team. Additionally, each team is required to produce a PowerPoint presentation that provides: background on the topic the team investigated, the approach taken in the scripting component of the project, and a discussion of both the approach and results of the pipeline component.

Those working on the writing component are responsible for both producing an introduction to the topic under investigation as well as working with their team members to thoroughly document the resultant code. 

Projects from last year can be found [here](<http://cbb752spring2016.github.io/>) and serve as a guide for the expected format.

Files related to Carl’s genome can be found [here](<https://zimmerome.gersteinlab.org/2016/05/06/part01_gerstein/>).

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

**Writing:** Disucss the difference of degree centrality and betweenness centrality you observed. How are these centralities measurement helpful for us to understand different mutations and the protein-protein network.

**Coding:** Calculate the degree centrality and betweenness centrality of proteins containing and not containing SNPs in Carl’s genome using a PPI file.

**Pipeline:** Use Cytoscape or other softwares to visualize the protein-protein network. Check the centrality calculations with the software and demonstrate one or two examples. Perform hierarchical network analysis and determine if there is enriched or depleted mutation in each hierarchy.

#### Part 4: Structure Analysis
**Please see the zip file available at http://cbb752b17.gersteinlab.org/homework for all relevant files and equations for part 4.**

**-1. Mutation F19Y is found in Karl Zimmer’s genome for 4BMB (galectin-8). Analyze the structure of this mutation.**

**Writing:** What changes has this mutation cause to the structure and what impact could the mutation have, from molecular pathway to the the phenotype? Read paper 1. Discuss the changes in protein structure and binding affinity caused by this mutation. Does this mutation cause changes in phenotype? In particular, discuss the changes seen in Figure 4.

**Coding:** We have used the wildtype structure to investigate how this mutation will change the protein. The files 4BMB_F19.txt and 4BMB_F19Y.txt contain the repulsive Lennard-Jones energy for each side chain dihedral angle combination of these two residues in the protein core of 4BMB. Plot the total potential energy involving interactions among side chain atoms as a function of chi 1 and chi 2. Discuss how much you expect the wildtype protein to change to accommodate this mutation.
A crystal structure exists for the F19Y mutation (4BME). Using the aligned files provided (4BMB_aligned.pdb, 4BME_aligned.pdb), calculate the root-mean-square deviation (rmsd) of the heavy atoms in the two structures. How might this rmsd be related to the stability of the protein?

**Pipeline:** Download the 4BMB structure from the Protein DataBank. Using the Rosetta Software Suite, generate 10 different protein mutations at location 19 (chosse 10 of the 20 amino acids). Obtain the relaxed protein structure following each mutation from Rosetta and compare the energy of the resulting structures. Which mutant is most stabilizing and which is most destabilizing? Why do you think this is the case?

**-2. Analyze the structure of another mutation of galectin-8 at location 35: I35F.**

**Writing:** What changes has this mutation cause to the structure and what impact could the mutation have, from molecular pathway to the the phenotype? Why would we expect the I35F mutation to be more detrimental to the protein than a mutation at location 19? Does this match what is found in the rmsd and energy calculations?

**Coding:** : Once again, we have used the wildtype structure to investigate this mutation. The files 4BMB_I35.txt and 4BMB_I35F.txt contain the repulsive Lennard-Jones energy for each side chain dihedral angle combination of these two residues in the core of 4BMB. Plot the total potential energy involving interactions among side chain atoms as a function of chi 1 and chi 2. Discuss how much you expect the wildtype protein to change to accommodate this mutation. A three-dimensional structure of I35F was generated using the Rosetta Software Suite. Using the aligned files provided (3VKO_H_aligned.pdb, 3VKO_H_I35F_aligned.pdb), calculate the root-mean-squared deviation of the heavy atoms in the two structures. How might this rmsd be related to the stability of the protein?

**Pipeline:** Download the 4BMB structure from the Protein DataBank. Using the Rosetta Software suite, generate 10 different protein mutations at location 35 (choose the same 10 amino acids as above). Obtain the relaxed protein structure following each mutation from Rosetta and compare the energy of the resulting structures. Which mutant is most stabilizing and which is most destabilizing? Why do you think this is the case? Are mutations at this location more or less deleterious than at location 19?


Paper 1: http://onlinelibrary.wiley.com/doi/10.1111/febs.12716/abstract

These links may be helpful for getting started with Rosetta:
http://2016.igem.org/wiki/images/5/59/Rosetta_Guide_for_the_iGEM_Beginner.pdf
https://www.rosettacommons.org/demos/latest/public/calculate_protein_protein_ddg/README
 
