
# LigScapeData

<!-- badges: start -->
<!-- badges: end -->

Stores LigScape's database of ligand intracellular transcriptomic signatures.  
LigScape is a comprehensive database of ligand-signatures to predict cell-cell communication.
Ligand-receptor interactions mediate intercellular communication, inducing transcriptional changes that regulate physiological and pathological processes. Ligand-induced transcriptomic signatures can be used to predict active ligands; however, the absence of a comprehensive set of ligand-response signatures has limited their practical application in predicting ligand-receptor interactions. To bridge this gap, we developed LigScape, a curated database encompassing intracellular transcriptomic signatures for human ligands. LigScape compiles signatures from published transcriptomic datasets and established resources, generating both gene- and pathway-based signatures for each ligand.
Using the LigScape database as a reference, we developed a companion computational tool that infers the ligands responsible for transcriptomic changes within receiver cells, and the corresponding cell-cell interaction networks between multiple cell types or clusters. 
We applied LigScape to predict active ligands driving transcriptomic changes in controlled in vitro experiments and real-world single-cell sequencing datasets. LigScape outperformed existing methods, achieving higher accuracy in identifying active ligands at both the gene and pathway levels. These results establish LigScape as a robust platform for ligand signaling inference, providing a powerful tool to explore ligand-receptor biology across diverse experimental and physiological contexts.

<hr>
\item sigmeta: a data.frame of manually curated meta.data of the LigScape ligand-signatures containing eight columns “sig_id”, “Ligand”, “Organism”, “Celltype.cellline”, “Dose”, “Duration”, “Platform”, and “source”.
\item siglist: a list of the LigScape ligand-signatures, in which each entry stores a signature, with the names of the list consistent with the row.names and the “sig_id” column of the data.frame “sigmeta”. 
\item lr_network: a data.frame of ligand(L)-receptor(R) pairs, each row represents an LR-interaction pair. The first four columns "L", "Lgene", "R", and "Rgene" represent ligand name (match the ligand names in LigScape), ligand gene symbol(s), receptor name, and receptor gene symbol(s), and the latter two columns “source” and “database” store the data sources and more general databases from which the LR pairs were collected. 
Remark: For a ligand or receptor with sub-units, say unitA and unitB, the gene symbols are connected by "_" in the L/Rgene column as "unitA_unitB".
\item mykegg: a list of gene-nodes in KEGG pathways. Each entry of mykegg is a vector of gene-symbols of the genes-nodes in a KEGG pathway.

<hr>

The companion R package for analyzing cell-cell communication is available at
[LigScape](https://github.com/yingxinac/LigScape/)






