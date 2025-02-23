
# LignatureData

<!-- badges: start -->
<!-- badges: end -->

## Stores Lignature database of ligand intracellular transcriptomic signatures. <br />
**A comprehensive database of ligand-signatures to predict cell-cell communication.** <br />
 <br />
Ligand-receptor interactions mediate intercellular communication, inducing transcriptional changes that regulate physiological and pathological processes. Ligand-induced transcriptomic signatures can be used to predict active ligands; however, the absence of a comprehensive set of ligand-response signatures has limited their practical application in predicting ligand-receptor interactions. To bridge this gap, we developed Lignature, a curated database encompassing intracellular transcriptomic signatures for human ligands. Lignature compiles signatures from published transcriptomic datasets and established resources, generating both gene- and pathway-based signatures for each ligand. <br />
Using the Lignature database as a reference, we developed a companion computational tool [Lignature](https://github.com/yingxinac/Lignature/) that infers the ligands responsible for transcriptomic changes within receiver cells, and the corresponding cell-cell interaction networks between multiple cell types or clusters. 

<hr>

**sigmeta**: <br />
a data.frame of manually curated meta.data of the Lignature ligand-signatures containing eight columns “sig_id”, “Ligand”, “Organism”, “Celltype.cellline”, “Dose”, “Duration”, “Platform”, and “source”.

**siglist**: <br />
a list of the Lignature ligand-signatures, in which each entry stores a signature, with the names of the list consistent with the row.names and the “sig_id” column of the data.frame “sigmeta”. 

**lr_network**: <br />
a data.frame of ligand(L)-receptor(R) pairs, each row represents an LR-interaction pair. The first four columns "L", "Lgene", "R", and "Rgene" represent ligand name (match the ligand names in Lignature), ligand gene symbol(s), receptor name, and receptor gene symbol(s), and the latter two columns “source” and “database” store the data sources and more general databases from which the LR pairs were collected. <br />
Remark: For a ligand or receptor with sub-units, say unitA and unitB, the gene symbols are connected by "_" in the L/Rgene column as "unitA_unitB".

**mykegg**: <br />
a list of gene-nodes in KEGG pathways. Each entry of mykegg is a vector of gene-symbols of the genes-nodes in a KEGG pathway.


<hr>

**The companion R package for analyzing cell-cell communication is available at**
[Lignature](https://github.com/yingxinac/Lignature/)






