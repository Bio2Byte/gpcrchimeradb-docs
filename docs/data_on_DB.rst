Data describing the Entries
===========================

Every Entry on GPCRchimeraDB has an "Entry page". Depending on the Entry, the amount of information varies.
The organization of the "Entry page" is the same for chimeric and natural entries.
You can easily navigate between the sections of the "Entry page" using the Sidebar.
Here, we discuss the different sections of the "Entry page" and the data they contain.


Overview
---------
In this section, a general description of the entries is given.
For Natural GPCRs, the information was directly retrieved form diverse databases as we will discuss below.
For Chimeric GPCRs, the information is the concatenation of the information of the two parents of the chimera.
It is always 1st the info from the extracellular (EC) parent and then 2nd from the intracellular (IC) parent.
The information is combined with either a "_" or a "&".

-   **Type of GPCR**: Either "Natural GPCR" or "Chimeric GPCR". The differences is explained in :ref:`input_sequences`.
-   **Pharmacological name**: From GPCRdb.
-   **Abbreviated name (or gene related name or UniProt name)**: from UniProt.
-   **ID**: From UniProt.
-   **Name(s)**: From UniProt. Provides name(s) that are commonly also used to describe the GPCR of interest.
-   **Organism**: From UniProt. The Scientific Name was converted to the Common Name using Python.
-   **Class**: From InterPro. For now only class A (Rhodopsin) GPCRs are on GPCRchimeraDB because of the lack of chimeras from other classes.
-   **Subclass (Ligand-based)**: From GPCRdb. This classification related to the type of endogenous ligand the GPCR binds.
-   **Subclass (Phylogenetically-based)**: Based on this `paper <https://doi.org/10.1371/journal.pcbi.1004805>`_ and extended using IQtree. It provides a classification based on a phylogenetical analysis and therefore, this is a more sequence based classification compared to the ligand-based subclass.
-   **Endogenous Ligands**: From GPCRdb.
-   **G-protein coupling**: From GPCRdb.
-   **β-arrestin coupling**: From GPCRdb.
-   **Structures**: From PDB (IDs identified based on UniProt ID), AlphaFoldDB and AlphaFold multistate (models based on AlphaFold but using labelled templates). For the Chimeras, as the AlphaFold models were not available, we have computed them in-house using AlphaFold2 and the default parameters. In this table you thus find both experimental 3D structures and predicted 3D models. The activation state of the 3D structures is determined by GPCRdb but is not available for all structures ("undetermined"). AlphaFold multistate models are provided by AlphaFold multistate themselves (L. Heo & M. Feig, 2022) and are therefore not available for all entries.


Schematic Description
---------------------
In this section, the information provided for the Natural and Chimeric Entries differ. Nevertheless, the information comes from the same source, the literature.

For the **Natural Entries**, we provide heatmaps colored based on the frequency a residue is a cutting point of chimeric designs.
In total there are 4 heatmaps as a Natural chimera can be either a EC or IC side parent and as it can either form a functional or non-functional chimera.
The number of chimeras evaluated to obtain a heatmap is indicated in the heatmap's title.
As the chimeras are often designed with the same parents, many Natural Entries have blank heatmaps, they are not invovlved in chimeric design.

For the **Chimeric Entries**, we provide a schematic description of the design and summarize its information extracted from the literature.
Please refer to :ref:`input_sequences` for a detailled description of the terminology used to describe chimeric GPCRs.
**About the functionality of the chimera:** It is important to highligh this feature as functionality is dependent on the functional assay that was performed to determine it.
Please refer to the journal article describing the chimera for more details about the conditions in which the chimera was found functional (or not).

Sequence Properties
-------------------
This section describes the GPCRs at the residue level. By default the following features are shown (if available for the GPCR of interest):


3D Structure
-------------
In this section, the different 3D structures or models listed in the "Structures" table in the Overview Section can be visualized. You can select the 3D structure you want to visualize in the dropdown list.
The user can interact with the structure by rotation the molecule. Zooming is also available. Note that the Sequence Properties and 3D Structure sections are connected. 
If you click on a residue of a 3D structure, a yellow vertical line will highlight the corresponding residue in the Sequence Properties section. The other way around also works: you can click on a residue in the Sequence Properties section and it will be automatically localized in the 3D structure.

**Gaps in 3D structures:** Experimental 3D structures can contain unresolved sections (mainly in their unstructured regions, i.e., loops). These sections are therefore not visible in these partially unresolved 3D structures but are of course present in their Sequence Properties section. 
For this reason, when you click on a residue in the Sequence Properties section, it is possible that it does not get localized in the 3D structure.
This is because it is not in the 3D structure, your residue is part of an unresolved region. 
Predicted 3D models do not have unresolved sections. Therefore, this will never happen with predicted 3D models.

Finally, you can color your 3D structure using the "change color scheme" button at the top of this section. The color schemes you can choose between are the following:
-   B-factor/pLDDt: If you are visualizing an experimentally resolved 3D structure, your 3D structure will be colored based on its B-factor. For the 3D models, its pLDDT will be utilized.
-   Cutting points (only for Chimeric Entries): color your 3D structure in funciton of the contribution of its two parents. Magenta is always used to color the sections of the EC side parent while cyan is used for the IC side parent.
-   Biophysical features (only for Chimeric Entries): see section above.
-   Delta (Δ) EC/IC side parent (only for Chimeric Entries): Difference in biophysical behavior between your Chimeric Entry and its EC/IC side parent. See section above.

Selected Residue
----------------

Other Chimeric Designs
----------------------