# Lipophilicity profiles of bioactive regions of HDPs

The context-dependent lipophilicity of each amino acid was computed using a pH-dependent and structure-based lipophilicity scale called ***ProtL scale***.

It is based on the *IEFPCM/MST continuum solvation method*, wherein the lipophilicity of each amino acid is calculated, considering its specific structural features and the pH of the medium. This methodology was implemented as reported in our previous work (https://pubs.acs.org/doi/10.1021/acs.jpclett.9b00028) according to Eq. 1

![image](https://raw.githubusercontent.com/cbio3lab/SAR_RECOMBINANT_HDPs/main/PICTURES/eq1.png)


Eq. 1 applies to any peptide composed of N amino acids, where $\lambda$ stands for the fraction of solvent-exposed surface area (SASA) of the amino acid, including the backbone (bb), side-chain (sc), and capping groups (cg) according to the local structural environment of the HDP domain. For our purposes, the SASA was determined using NACCESS program. The   factor accounts for a correction due to the burial of the side chain of hydrophobic residues (Ala, Leu, Ile, Val, Pro, Phe, Trp, Met, and Tyr) from water to a lipophilic environment. This contribution has been estimated to be 0.023 kcal mol−1 Å−2 according to the studies reported by Moon and Fleming for the transfer of nonpolar side chains from water into a lipid bilayer (https://www.pnas.org/doi/full/10.1073/pnas.1103979108). Therefore, the $\betta$ term had been estimated from the fraction of the buried side chain concerning the fully buried side chain 




