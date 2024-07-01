Data describing the Entries
===========================

Every Entry on GPCRchimeraDB has an "Entry page". Depending on the Entry, the amount of information varies.
The organization of the "Entry page" is the same for chimeric and natural entries.
You can easily navigate between the sections of the "Entry page" using the Sidebar.
In this section we discuss the different sections of the "Entry page" and the data they contain.


Overview
---------
In this section, a general description of the entries is given.
For Natural GPCRs, the information was directly retrieved form diverse databases as we will discuss below.
For Chimeric GPCRs, the information is the concatenation of the information of the two parents of the chimera.
It is always 1st the info from the extracellular (EC) parent and then 2nd from the intracellular (IC) parent.
The information is combined with either a "_" or a "&".

-   Type of GPCR: Either "Natural GPCR" or "Chimeric GPCR". The differences is explained in :ref:`input_sequences`.
-   Pharmacological name: From GPCRdb.
-   Abbreviated name (or gene related name or UniProt name): from UniProt.
-   ID: From UniProt.
-   Name(s): From UniProt. Provides name(s) that are commonly also used to describe the GPCR of interest.
-   Organism: From UniProt. The Scientific Name was converted to the Common Name using Python.
-   Class: From InterPro. For now only class A (Rhodopsin) GPCRs are on GPCRchimeraDB because of the lack of chimeras from other classes.
-   Subclass (Ligand-based): From GPCRdb. This classification related to the type of endogenous ligand the GPCR binds.
-   Subclass (Phylogenetically-based): Based on this `paper <https://doi.org/10.1371/journal.pcbi.1004805>`_ and extended using IQtree. It provides a classification based on a phylogenetical analysis and therefore, this is a more sequence based classification compared to the ligand-based subclass.
-   Endogenous Ligands: From GPCRdb.
-   G-protein coupling: From GPCRdb.
-   β-arrestin coupling: From GPCRdb.
-   Structures: From PDB (IDs identified based on UniProt), AlphaFoldDB and AlphaFold multistate. For the Chimeras, as the AlphaFold models were not available, we have computed them in-house using AlphaFold2 and the default parameters.


Schematic Description
---------------------
.. In this section, the information provided for the Natural and Chimeric Entries differ.

.. For the Natural Entries we provide heatmaps colored based on the frequency a residue is a cutting point of a chimeric desing.
.. In total there are 4 heatmaps as a Natural chimera can be either a EC or IC side parent and as it can either form a functional or non-functional chimera.
.. The number of chimeras evaluated to obtain a heatmap is indicated in the heatmap's title.
.. As most of the chimeras are 

Sequence Properties
-------------------

3D Structure
-------------

Selected Residue
----------------

Other Chimeric Designs
----------------------