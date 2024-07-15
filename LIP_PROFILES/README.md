# Lipophilicity profiles of bioactive regions of HDPs

The context-dependent lipophilicity of each amino acid was computed using a pH-dependent and structure-based lipophilicity scale called ***ProtL scale***.

It is based on the *IEFPCM/MST continuum solvation method*, wherein the lipophilicity of each amino acid is calculated, considering its specific structural features and the pH of the medium. This methodology was implemented as reported in our previous work (https://pubs.acs.org/doi/10.1021/acs.jpclett.9b00028) according to **Eq. 1**

![image](https://raw.githubusercontent.com/cbio3lab/SAR_RECOMBINANT_HDPs/main/PICTURES/eq1.png)


**Eq. 1** applies to any peptide composed of N amino acids, where **$\lambda$** stands for the fraction of solvent-exposed surface area (SASA) of the amino acid, including the backbone (bb), side-chain (sc), and capping groups (cg) according to the local structural environment of the HDP domain. For our purposes, the SASA was determined using NACCESS program. The   factor accounts for a correction due to the burial of the side chain of hydrophobic residues (Ala, Leu, Ile, Val, Pro, Phe, Trp, Met, and Tyr) from water to a lipophilic environment. This contribution has been estimated to be 0.023 kcal mol<sup>-1</sup>Å<sup>-2</sup> according to the studies reported by Moon and Fleming for the transfer of nonpolar side chains from water into a lipid bilayer (https://www.pnas.org/doi/full/10.1073/pnas.1103979108). Therefore, the **$\beta$** term had been estimated from the fraction of the buried side chain concerning the fully buried side chain.

In this version of the calculation of context-dependent lipophilicity of amino acids, two correction factors were introduced:

i) an adjustment in the **$\alpha$** term

ii) an additional correction factor, **$\gamma$** 

Initially, the parameter **$\alpha$** introduced a correction to the hydrophobic contribution when the backbone participates in a hydrogen bond (HB). However, in the new algorithm proposed in **Eq. 1**, the factor **$\alpha$** also incorporates the hydrophobic contribution due to the side-chain intramolecular hydrogen bonds. This contribution can be estimated to amount, on average, to 0.73 (log P units) per HB. 

Finally, the **$\gamma$** factor accounts for the enhancement of the amino acid's lipophilic character due to the formation of salt bridges. This electrostatic interaction has been experimentally shown to increase the transfer of oppositely charged side chains in model peptides in n-octanol/water systems by up to ca. 4 logP units relative to glycine. Additionally, it stabilizes the presence of charged residues in highly hydrophobic environments, such as transmembrane helices. Stabilization in both immiscible solvent systems and transmembrane proteins has demonstrated a consensus value of about 1 logP unit (approximately 1 kcal/mol) compared to the cost of transferring these ionic side chains individually without interacting with each other. In this framework, for consistency with our calculations, the n-octanol/water partition coefficient of non-interacting pairs of oppositely charged amino acid side chains is around -9 logP units. This suggests that to stabilize these pairs in hydrophobic environments by at least 1 logP unit (0.5 logP units by residue), the interaction must favor the transfer to n-octanol by at least 10 logP units. In this way, the value adopted for **$\gamma$** in each amino acid forming a salt bridge is approximately 5 logP units. For special cases involving a three-body interaction, where the same charged side chain participates in two salt bridges, a **$\gamma$** value of 7 logP units was established for the amino acid that interacts twice to achieve an additional global stabilization of 2 logP units (1 logP unit by pair). These extra logP units compared to a two-body interaction are supported by evidence indicating that three-body intermolecular interactions in proteins, e.g., cation-**$\pi$**-cation interactions, exhibit greater stability than the simple additive assumption.


Thus, the CSV files with the lipophilicity profiles in the HDPs contains:

**1. id:** The identifier for each amino acid in the *pdb structure* of the HDPs (see STRUCTURES folder).

**2. res:** The three-letter code of each amino acid.

**3. pHcol:** The pH at which the lipophilicity calculation was made.

**4. logD_M1:**

**5. sf:**

**6. sasresi:**

**7. f:**

**8. sfsc:**

**9. sassc:**

**10. fsc:**

**11. hbbb:**

**12. hbsc:**

**13. hpeDB:**

**14. sb:**

**15. logD_M2:**

**16. logD_M3:**

**17. logD_M4:**

**18. logD_M5:**
