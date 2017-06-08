---
layout: page
title: CBB752 Spring 2017
tagline: Final Project 4.2
---

A Study of the Effects of Mutations at A-I35 in Human Galectin-8 

------------------


Table of Contents
1. Introduction
2. Writing
   1. The I35F Mutation
   2. Additional Mutations to I35
   3. Conclusion
3. Coding
   1. Documentation
   2. Results
4. Pipeline
   1. Documentation
   2. Results
   3. Files
5. References


-----------------------




**Contributors**

 -Writing: Megan Brady
 
 -Coding: Amber Jessop
 
 -Pipeline: Krystle Reiss

### Introduction:

Galectin-8 is a type of human galactin; these proteins have a carbohydrate recognition domain (CRD) and have the ability to bind to β-galactose (Cummings and Liu, 2009). Galectin-8, as a tandem repeat galactin, has two CRDs linked together by a small peptide, with each CRD binding to a different polysaccharide. In the extracellular matrix, Galectin-8 can tightly bind integrins and a CD44 variant, and contributes to their role in signaling and interactions (Cummings and Liu, 2009). It has also been implicated with tumors, with roles in controlling endothelial cell migration and angiogenesis (Troncoso et al. 2014). 
	
The size and the polarity of amino acids are important in the overall structure of the protein, and amino acid mutations affecting these traits are likely to disrupt the structure and function. The core of the protein often contains hydrophobic and nonpolar residues, while the surface of the molecule is more likely to contain polar residues (Lins et al. 2003). This feature is critical to the overall fold of the protein, as the hydrophobic effect is important in the packing of the protein core. Therefore, mutations within the core that change the polarity of the amino acid are expected to be extremely deleterious, as they have the potential to disrupt this tight, hydrophobic packing. Any mutations that affect the shape of an amino acid within this hydrophobic core also has the potential to greatly disrupt the structure, as the interacting residues are forced to compensate for extra space that is required by a larger residue or for the space and interactions missing from a smaller residue. 
	
The software ROSETTA is a groundbreaking program that can be used in protein structure prediction, protein-protein or protein-ligand docking, conformational sampling, protein design, as well as protein energy simulations (Kaufmann et al. 2010). It can therefore be used to analyze potential mutations of a protein, as it determines the energy that a resultant mutant structure would have in comparison to the original protein. In performing the energy calculations, the program either considers the side chains to be centroids, in which solvation, electrostatics, and hydrogen bond information is included in the calculation, or considers the side chains to be super atoms, which incorporates the Lennard-Jones potential, solvent effects, electrostatic effects, and amino acid free energy into the calculation (Kaufmann et al. 2010). As both techniques include statistical and physical potentials, the resultant energies are in units of “ROSETTA energy units”, with lower energies corresponding to more benign and allowed mutations.

### Writing:

The I35F Mutation

A mutation within the 4BMB gene encodes a galactin-8 protein with a I35F mutation. Both isoleucine and phenylalanine are nonpolar amino acids, and so the presence of these side chains would likely not disrupt the overall hydrophobic packing. However, unlike isoleucine, the phenylalanine has a large and bulky ringed side chain. Therefore, this I35F mutation would be expected to affect some of the interactions within the core, as interacting residues are forced to compensate for the additional density, and could have a detrimental effect on the overall structure of the protein. When computing the ROSETTA structure corresponding to this mutation, this mutation was in fact determined to be harmful, as it increases the energy by 4.821 REUs. 

The impact of the I35F mutation can also be analyzed through looking at the potential energy of side chain atoms, as plotted against the possible χ1 and χ2 bond angles. In the wild type protein (I35), the lowest potential energy of interaction occurs around 180° for χ1 and 300° for χ2. However, there is also a low potential from a χ1 value between 120° and 200° and a χ2 value between 260° and 340°. This results in a large range of angles possible for the two side chains that would result in low potential energy. In contrast, the I35F structure contains a very restrained plot of potential energy. In this case, the lowest potential energy occurs at 70° (χ1) and 270° (χ2). Not only is this the only orientation which has a low potential energy, but this “low” potential energy is around 133 units, while the values in the wild type are less than 0.8 units. This indicates that the I35F mutant would be extremely constrained in comparison to the wild type and that its lowest possible potential is still substantially higher than is possible with the wild type, both which suggest that this mutation would be extremely unfavorable and damaging to the protein. 

The heavy atoms of both the wild type and I35F mutant can be compared, and can indicate overall changes to the structure that could occur to accommodate the mutation. The overall RMSD is 0.591, signifying that the I35F variant does force the other proteins to change their positions to account for its additional size. This displacement is largest in the mutated residue itself, as well as in residues 59, 71, 72, 98, and 104. The large RMSD of these residues (which are mostly on the surface) indicate that they have to greatly change their orientation to accommodate the mutation, likely destabilizing the protein and making this particular variant extremely disfavored. 

Additional Mutations to I35

Other mutations to I35 that change the size, but not the charge, of the residue in question include I35G, I35A, I35V, and I35M. Glycine is significantly smaller than isoleucine, and has the potential to disrupt this hydrophobic interaction network. This is confirmed through the ROSETTA analysis, as this change increases the energy by 1.013 REU, suggesting that mutation would have a slight deleterious effect. I35A decreased the energy by 1.097 REU, signifying a small benefit to this mutation, while I35V results in a decrease in energy of 2.775 REU, and as such is the most favorable of the I35 mutations investigated. This isoleucine to valine mutation is quite common, and it makes sense that the similarities in size and hydrophobicity result in a stable and allowed mutation. Interestingly, the I35L mutation only decreased the energy by 1.712 REU, and was therefore not as stable as the valine mutation, though leucine has the exact same number of atoms as isoleucine. The presence of the additional Cγ in leucine can extend into the pocket formed by V48 and I146, creating additional interactions that make this mutation favorable, though still less favorable than the I35V mutation. The I35M mutation resulted in a ROSETTA energy of 2.087 REU, and as such is a destabilizing mutation. It is logical that this mutation would increase the energy, as the presence of a large sulfur atom and the extended nature of the side chain do not fit nicely into the core, disrupting the hydrophobic interaction network. 

Mutations were made to I35 that affected the charge of the residue, including I35E, I35D, and I35R. Both glutamate and aspartate contain negatively charged side chains, and would be expected to disrupt the hydrophobic interactions. However, while I35D is an unfavorable mutation that increases the energy by 1.887 REU, I35E is a highly favorable mutation, decreasing the energy by 2.652 REU. This surprising result can likely be explained by the presence of a pocket between V48 and I146; the longer side chain present in glutamate has the ability to extend into this crevice, allowing it to not disrupt the overall structure. Aspartate cannot fit into this spot, and instead disrupts the surrounding interactions. The I35R mutation was extremely disfavorable, increasing the energy by 11.913 REU. In this case, the extended side chain clashes with F46, disrupting the typical hydrophobic interactions within the region and greatly decreasing the stability of the protein. 

Proline, with its unique structure, can often introduces clashes and tension into the protein. Surprisingly, however, the I35P mutant slightly decreases the energy by 0.115 REU. This is because while creating some strain on the backbone side chain, the presence of the three carbon groups is similar to the four-carbon side chain seen in isoleucine. This allows for the molecule to fit well into the core, as these hydrophobic side chains do not clash with the other residues within the hydrophobic core.  

The mutation I35Y changes both the size of the residue, as well as adding a polar side chain. As tyrosine and phenylalanine have similar structures, with a hydroxyl group added to the benzene ring in tyrosine, one would expect the mutation I35Y to have a similar or greater disfavorability to I35F. However, while I35F increased the energy, I35Y actually decreased the energy by 2.660 REU. This is likely due to the fact that in the I35Y mutant, the residue L138 is moved away from the tyrosine by around 1Å, due to the presence of its polar group. This creates space for the tyrosine to fit, allowing its benzene ring to contribute to some of the hydrophobic interactions, and results in an overall favorable mutation. This movement of L138 was not seen with the I35F mutation, as there was no difference in polarity causing the leucine to move, and as such just disrupted these interactions and led to an increase in energy.

Conclusion

A single amino acid change has the potential to greatly affect the protein through its interactions with surrounding residues. This is seen with the mutation I35F, as the larger size of the phenylalanine results in less side chain conformations and a higher energy potential than the wild type. Other mutations, such as I35E, I35V, and I35Y have the ability to fit within existing grooves or to move residues that would result in potential clashes, and as such these mutations can be considered benign. In addition to I35F, other mutations are also harmful, including I35R and I35D, as they disrupt the tight hydrophobic packing present in the core. Differences in energy between fairly similar mutations, such as D/E and F/Y, signify that it is important to consider the entire protein during deleteriousness predictions, and to not simply assume whether a mutation will be acceptable based only on its size and charge. The residues interacting with the mutation site have differing abilities to compensate for the change, and as such these interactions are important to consider and are critical to the classification of the mutation. 


### Coding:


#### Documentation:
Two python scripts are provided to compare the structure of the mutant and wild type structures:  mut_energy.py and mut_rmsd.py. 
The first takes in two files: ‘Wildtype.txt’ and ‘Mutant.txt’, each of which has Repulsive Lennard-Jones energies as a function of side-chain dihedral angles for the native human Galectin 8 and (with an isoleucine at site 35) and it’s mutation I35F. The output of mut_energy.py is a set of two figures that show sterically allowed side-chain dihedral angle combinations.
The second script, mut_rmsd.py takes in two aligned .pdb files (generated with Rosetta Software Suite): mut.pdb and wt.pdb. It generates a plot of distance between corresponding heavy atoms of the two 3D structures and calculates the root-mean-square displacement (RMSD). 


#### Results:
For the wild type structure (see below), there are significantly more sterically allowed side chain dihedral angles. The mutant protein, with a phenylalanine residue that is significantly larger than the isoleucine, shows a very narrow range of allowed configurations. While the allowed angle distribution of I35F overlaps the allowed region for I35, the clashing energies for I35F is on the order of 100 times larger than the energies of I35, indicative of a relatively unstabilized structure.

![image](https://github.com/CBB752Spring2017/final-project-4-2-team-4-2-1/blob/master/wt4bmb.png)
![image](https://github.com/CBB752Spring2017/final-project-4-2-team-4-2-1/blob/master/mut4bmb.png)

The RMSD for the I35 vs. I35F structures was found to be 0.591 angstrom, but a plot of the distances between corresponding heavy atoms reveals that there are some notable differences in atom position at a few different residues. In this analysis, atoms that are on the side chain of the mutation residue were excluded since there is not a direct correlation between them. How ever the atoms of the mutation site back bone are included. The figure below was generated with PyMol software (red is the mutant and blue is the wild type residue) for a visual on the difference between the two residues.

![alt text](https://github.com/CBB752Spring2017/final-project-4-2-team-4-2-1/blob/master/res35zoom.png)

Included in these is, not surprisingly, residue 36. Others are residues 71 and 72, which are surface residues and point away from the core. 
![alt text](https://github.com/CBB752Spring2017/final-project-4-2-team-4-2-1/blob/master/distance.png)

Below is another figure generated with PyMol, showing the similarity of the two structures (red: mutant, blue: wild type). Residues 71 and 72 can be seen at the bottom, right of center).

![alt text](https://github.com/CBB752Spring2017/final-project-4-2-team-4-2-1/blob/master/overlayWhole.png)


### Pipeline:
Multiple mutations at location 35 in chain A of protein 4BMB were evaluated using the Rosetta software package.

#### Documentation:
The protein structure 4BMB (Ruiz 2014) was acquired from the Protein Database. The Rosetta software package was used to create eleven
mutations at location 35 in chain A. These mutations were I35A, I35D, I35E, I35F, I35G, I35L, I35M, I35P, I35R, I35V, and I35Y. The
native protein and all mutations were optimized with Rosetta's Relax application (Nivón 2013) using the full atom and quick options. The
energies of these relaxed structures were calculated with Rosetta's Score application (O'Meara 2015), also using the full atom option.

#### Results:
Results were somewhat surprising. While the most and least stable mutation (valine and arginine, respectively) were predicatable, there 
were several unexpected results, such as the drastic energy differences between tyrosine and phenylalaline, the latter of which was very
unstable compared to the fore). It is thought that a slight shift in a nearby residue caused by the additonal hydroxyl group on tyrosine
was the cause for this disparity, although why this shift makes I35Y more stable than the native structure is unclear. The overlapping
structures of I35F and I35Y can be seen below. I35F carbons are colored yellow and I35Y are pink.
![alt text](https://github.com/CBB752Spring2017/final-project-4-2-team-4-2-1/blob/master/I35YF_overlay.png)
There was no overall trend as to what made certain mutations more stable than others (e.g. size, hydrophobicity, charge), but some minor
trends were present. For example, residues that have sidechains that are three carbon long (glutamate and leucine) are more stabilizing
while residues that are shorter (alanine, aspartate, etc.) or longer (arginine and methionine) are less stable. The reason for this may
be a pocket between V48 and I146 that is stabilized by when it is filled (as with glutamate and leucine). However, a residue that is too
long, like arginine, clashes with the nearby residue F46.

#### Files:
Rosetta Score Output: score.sc

Scores with Differences: 4bmb_I35_mutation_scores.xlsx

Native Structure: 4bmb_0001.pdb

Mutant Structures: 4bmb.A-I32X_0001.pdb ('X' is replaced with the mutant amino acid's 1-letter abbreviation)

Images: I35X.png ('X' is replaced with the mutant amino acid's 1-letter abbreviation or omitted for native structure)

Overlay of I35Y and I35F: I35YF_overlay.png


### References:

Cummings RD, Liu FT. Galectins. In: Varki A, Cummings RD, Esko JD, et al., editors. Essentials of Glycobiology. 2nd edition. Cold Spring Harbor (NY): Cold Spring Harbor Laboratory Press; 2009. Chapter 33.

Kaufmann KW, Lemmon GH, DeLuca SL, Sheehan JH, Meiler J. Practically Useful: What the Rosetta Protein Modeling Suite Can Do for You. Biochemistry. 2010;49(14):2987-2998. 

Lins L, Thomas A, Brasseur R. Analysis of accessible surface of residues in proteins. Protein Science : A Publication of the Protein Society. 2003;12(7):1406-1417.

Nivón, L. G., Moretti, R., and Baker, D. (2013) A Pareto-Optimal Refinement Method for Protein Design Scaffolds. PLoS ONE 8.

O’Meara, M. J., Leaver-Fay, A., Tyka, M. D., Stein, A., Houlihan, K., Dimaio, F., Bradley, P., Kortemme, T., Baker, D., Snoeyink, J.,
 and Kuhlman, B. (2015) Combined Covalent-Electrostatic Model of Hydrogen Bonding Improves Structure Prediction with Rosetta. Journal of
 Chemical Theory and Computation 11, 609–622.
 
Ruiz, F. M., Scholz, B. A., Buzamet, E., Kopitz, J., André, S., Menéndez, M., Romero, A., Solís, D., and Gabius, H.-J. (2014) Natural 
 single amino acid polymorphism (F19Y) in human galectin-8: detection of structural alterations and increased growth-regulatory activity 
 on tumor cells. FEBS Journal 281, 1446–1464.
 
 Troncoso, M. F., Ferragut, F., Bacigalupo, M. L., Delgado, V. M. C., Nugnes, L. G., Gentilini, L., Laderach, D., Wolfenstein-Todel, C., Compagno, D., Rabinovich, G. A., Elola M. T.; Galectin-8: A matricellular lectin with key roles in angiogenesis. Glycobiology 2014; 24 (10): 907-914. 

