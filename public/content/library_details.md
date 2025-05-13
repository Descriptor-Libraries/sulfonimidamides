# Library Details

## Molecule Identification
Given the lack of commercially available racemic sulfonimidamides, chemists generated a list totaling 117 diverse, synthetically-feasible sulfonimidamides. These included aryl, benzylic, allylic, alkyl, alkenyl, and alkynyl sulfonimidamides with various halide substitutions, heteroatom containing rings, and substitution patterns.

## Conformational Searching & Conformer Selection

To capture the conformational flexibility of the substrates at a reasonable a computational cost, each sulfonimidamide was subject to a gas phase molecular mechanics conformational search using Schrödinger MacroModel and the OPLS4 force field.  An ensemble of conformers within 21 kJ/mol (5.02 kcal/mol) of the minimum were collected, excluding mirror-image conformers. 

If the ensemble consisted of greater than 20 conformers, the number of conformers was reduced by atomic root mean square deviation (RMSD)-clustering to the minimum Kelley penalty value and taking the centroids of the resultant clusters. The Kelley index facilitates selection of the optimal number of clusters and ensures the selected conformers structurally diverse.

## DFT Computations

All DFT geometry optimizations and sequent frequency calculations (Gaussian 16, rev C.01) were performed at the B3LYP-D3(BJ)/6-31G(d,p)-LANL2DZ(I) level of theory. The corresponding geometries were used for a series of single-point energy calculations at the M06-2X/def2-TZVP-SDD(I) level of theory. 

From the DFT calculations, global, atomic, and bond-level properties were collected for each conformer using [Get Properties](https://github.com/SigmanGroup/Get_Properties). 

Atoms in the sulfonimidamide functional group were consistently numbered as shown below, and the numbers are referenced in the descriptor names.

<div class="centered-container">
     <img src="content/sulfonimidamide_atom_numbering.png" alt="Sulfonimidamide Atom Numbering">
</div>

The dynamic range of properties across the conformational ensemble of a single sulfonimidamide was summarized by using five condensed measures for each of the properties.

| Descriptor              | Definition                                                                                      |
| ----------------------- | ------------------------------------------------------------------------------------------------|
| Boltz                   | Boltzmann-weighted average of a property from all the conformers in an ensemble (T = 298.15 K)  |
| max                     | highest value of a property given by any conformer in an ensemble                               |
| min                     | lowest value of a property given by any conformer in an ensemble                                |
| low_E                   | value of a property from the lowest energy conformer in the ensemble                            |
| range                   | absolute value of the max - min property value within an ensemble                               |

An extended explanation of the computational workflow used to build the sulfonimidamide library, as well as details on the collected and predicted descriptors can be found in the original publication supporting information.

## Citation
**Workflow:** van Dijk, L.; Haas, B. C.; Lim, N.-K.; Clagg, K.; Dotson, J. J.; Treacy, S. M.; Piechowicz, K. A.; Roytman, V. A.; Zhang, H.; Toste, F. D.; Miller, S. J.; Gosselin, F.; Sigman, M. S. Data Science-Enabled Palladium-Catalyzed Enantioselective Aryl-Carbonylation of Sulfonimidamides. *J. Am. Chem. Soc.* **2023**, *145*, 20959–20967. DOI: [10.1021/jacs.3c06674](https://doi.org/10.1021/jacs.3c06674)

**Updated PCA:** Haas, B. C.; Lim, N.-K.; Jermaks, J.; Gaster, E.; Guo, M. C.; Malig, T. C.; Werth, J.; Zhang, H.; Toste, F. D.; Gosselin, F.; Miller, S. J.; Sigman, M. S. Enantioselective Sulfonimidamide Acylation via a Cinchona Alkaloid-Catalyzed Desymmetrization: Scope, Data Science, and Mechanistic Investigation. *J. Am. Chem. Soc.* **2024**, *146*, 8536–8546. DOI: [10.1021/jacs.4c00374](https://doi.org/10.1021/jacs.4c00374)