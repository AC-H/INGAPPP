# INGAPPP
Analysis of bulk RNAseq data, differential expression using LME.

This R project contains the code to generate Figures for the publication titled:
Transcriptional signature of islet neogenesis-associated protein peptide-treated rat pancreatic islets reveals induction of novel long non-coding RNAs
URL:
https://www.frontiersin.org/articles/10.3389/fendo.2023.1226615/full?&utm_source=Email_to_authors_&utm_medium=Email&utm_content=T1_11.5e1_author&utm_campaign=Email_publication&field=&journalName=Frontiers_in_Endocrinology&id=1226615

The project can be started in RStudio by executing the file Taka_A1_A2_only.Rproj. The folder structure is as follows:
- **bash/** contains the code to align, quantify and generate new reference annotatios data using HISAT and Stringtie. Bash_coverageTables.TXT and Bash_Hisat_allTissues.TXT used to generate new reference and converage tables.
    
- **bin/** contains the R scripts to run the project. The number in front of the file name indicates the order in which the code should be executed, i.e. start with 01_PCA_script.R to get PCA associated figures, then 02_PCA_3D.R, 03_Heatmap.R, and 04_PCA_Heatmap_ClustBoxplot.R. 05_Wilcoxon_test.R contains statistical test functions used for the data. 

- **data/** contains the data for the project. The counts files are contained in the **counts** folder. All the data associated with the project is saved and loaded from here.
- **sc_analysis/** contains bash code to use CellRanger to create rat custom reference and the alignments of downloaded data from the Gene Expression Omnibus (GEO) with accession GSE84133. marcadores_RevFinal.csv contains main markers to identify most important cell types in pancreas.
- **works/** contains the posters associated with publication.

With regards to data exclusion, the 2 main points are noteworthy. The counts data contains cells from the so called EMP gate. These are erythromyeloid progenitors that were acquired and analyzed with the data, but not shown in the paper as the final focus was on A1 and A2 cells. Furthermore, some cells appeared to be damaged. These cells are documented in the file data/damaged-cells.csv and were excluded before running the Seurat algorithm.

The code is deposited on github under: https://github.com/AC-H/INGAPPP

In case of questions, please reach out to me at any time under acheidenreich@fbmc.fcen.uba.ar
