Designing a Novel Chimera with GPCRchimeraDB
=============================================

This section describes how to use GPCRchimeraDB to guide the design of a novel chimera involving **GPCRx**, the GPCR under investigation. The design process starts with selecting the appropriate design type (Type 1, 2, or 3, see manuscript), which determines whether GPCRx will serve as the **EC** or **IC** parent of the chimera:

- **Type 1 or 2**: Used for studying the functionality or signaling pathway of GPCRx. In this case, GPCRx will be the **IC parent**.
- **Type 3**: Used for uncovering the 3D structure or conducting ligand screening of GPCRx. Here, GPCRx will be the **EC parent**.

The next step is selecting **GPCRy**, the second parent. GPCRy should be a well-characterized receptor that complements gaps in knowledge about GPCRx. Depending on the design type:

- For **Type 1 or 2**, GPCRy should have a known ligand.
- For **Type 3**, GPCRy should have a known stabilizing effector.

Finally, the **cutting sites** in both GPCRx and GPCRy must be carefully determined to ensure that the resulting chimera can activate and successfully transmit the signal from the outside to the inside of the cell.

GPCRchimeraDB facilitates each stage of this design process, as outlined in the following steps:

Step 1: Explore the Entry Page of GPCRx
----------------------------------------

Each entry page in GPCRchimeraDB integrates annotations from major databases, providing an overview for further analysis. This includes:

- **Mutation impact**: Reviewing known mutations and their effects.
- **Evolutionary score**: Comparing GPCRx to its subclass.
- **Motif conservation**: Identifying regions that are sensitive to mutations.
- **PTM sites and interacting residues**: Understanding their role in GPCRx function.

Since chimeric design introduces stretches of mutations, understanding these factors is critical. The **1D-3D viewer** (:ref:`sequence_structure_viewer`) allows direct examination of key residues in their 3D context.

Step 2: Define Potential GPCRy Candidates
------------------------------------------

Selecting an appropriate **GPCRy** depends on the design type:

- For **Type 1** and **Type 3** chimeras, **GPCRy** is usually **Rhodopsin** and the **κ-Opioid receptor**, respectively.
- For **Type 2** chimeras, multiple candidates may be suitable. To identify GPCRy, consider:

  - **Well-characterized receptors**: Avoid orphan GPCRs (use the ligand-based subclass filter).
  - **Phylogenetic similarity**: Chimeras between related GPCRs tend to be more successful (filter by subclass).
  - **G protein compatibility**: Select a GPCRy that either binds the same or a different G protein as GPCRx.
  - **Previous chimeric designs**: Check past chimeras involving GPCRx or related receptors.
  - **Experimental feasibility**: Avoid receptors with regulatory or experimental constraints (e.g., opioid-related GPCRs).

Once suitable **GPCRy** candidates are identified, their entry pages should be explored (as in Step 1) to gain insights into their key residues.

Step 3: Determine Cutting Sites
-------------------------------

Cutting sites for GPCRx and GPCRy must be carefully chosen to enhance chimera design success. Based on literature, the following guidelines are recommended:

- **Preserve microswitches**: Ensure that essential microswitches for the **EC parent** remain intact.
- **Maintain secondary structure**: Introduce cutting sites within regions that share the same secondary structure.
- **Favor the EC parent**: The chimeric sequence should resemble the EC parent as closely as possible.
- **Preserve G protein binding**: The **IC parent** should contribute residues responsible for G protein binding.

Step 4: Optimize Cutting Sites Using Related Chimeras
------------------------------------------------------

Beyond the basic cutting site rules, analyzing previously designed chimeras can refine the selection process. GPCRchimeraDB offers tools for:

- **Comparing biophysical profiles**: Use the **1D-3D viewer** to compare a chimera’s biophysical profile to its parents.
- **Examining residue conservation**: Use the *Conservation parent vs chimera* track or `alignment tool <https://www.bio2byte.be/gpcrchimeradb/gpcrchimeradb/sequence_alignment_entries>`_.
- **Reviewing past cutting sites**: Identify how far previous cuts extend into TM helices.
- **Aligning parent 3D structures**: Download and superimpose 3D structures to find equivalent regions for cutting sites.

To **increase the likelihood of success**, **in silico validation** is recommended:

- **Structural modeling**: Generate an **AF2** or **ESMF** model and compare it to the 3D structures of GPCRx and GPCRy.
- **Confidence metrics**: Compare the chimera’s **pLDDT** and **PAE** values with its parent models.
- **Biophysical analysis**: Use `b2btools <https://bio2byte.be/b2btools/>`_ to ensure the chimera's properties align with natural GPCR behavior.
- **Molecular Dynamics (MD) simulations**: To be considered.
