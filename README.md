# DGE-Analysis-GSE152641-RNA-Seq-Data-Significant-Genes-via-edgeR-Galaxy-Server
DGE Analysis and Identification of Statistically Significant Genes in RNASequencing Data GSE152641 using edgeR on the Galaxy Main Server (usegalaxy.org)
Based on the complete workflow we executed, here is the full, ready-to-copy README.md file for your GitHub repository.

This file provides the necessary context, methodology, and a summary of the analysis steps and results.

DGE Analysis of GSE152641 RNA-Seq Data: Significant Genes via edgeR/Galaxy.

This repository documents and stores the results of a Differential Gene Expression (DGE) analysis comparing gene expression profiles in whole blood from COVID-19 patients versus Healthy Controls.

The analysis was performed entirely using the edgeR statistical package through the Galaxy Main Server (usegalaxy.org) interface.

🔬 Dataset Details
Parameter,Value
GEO Accession,GSE152641
Title,Transcriptomic Similarities and Differences in Host Response between SARS-CoV-2 and Other Viral Infection
Organism,Homo sapiens
Experiment Type,Expression profiling by high throughput sequencing (Bulk RNA-Seq)
Samples Analyzed,86 total samples (62 COVID-19 patients and 24 healthy controls)
Original Publication,Thair SA et al. iScience (2021)
The original study profiled peripheral blood to understand similarities and differences in the host response to SARS-CoV-2 compared to other acute viral infections.

💻 Methodology

The differential expression was determined using the edgeR package on the Galaxy platform, which is optimized for count-based RNA-Seq data.

Workflow:

    Data Input: The pre-processed count matrix (GSE152641_Inflammatix_COVID19_counts_entrez.csv) was uploaded alongside a custom metadata file (GSE152641 Metadata.csv) defining the Group factor.

    Analysis: The edgeR tool was run, specifying the contrast as COVID_19-Control using a single Count Matrix input.

    Filtering: The statistical results were filtered to identify genes meeting the required thresholds:

        Statistical Significance: FDR<0.05 (False Discovery Rate)

        Log Fold Change: ∣logFC∣>0.5 (Used to filter for biologically relevant magnitude)

    Visualization: A final Volcano Plot was generated to summarize the statistically significant gene expression changes.

📈 Key Results and Files

The main outcome of the analysis is the list of genes showing significant changes in the COVID-19 group relative to the Control group.
File Name,Description,Purpose
edgeR_COVID_19-Control.tsv,"Primary Results Table. Contains logFC, PValue, and FDR for all ∼20,000 genes.",Used for all subsequent filtering and visualization steps.
Galaxy17-[Scatterplot on dataset 15].pdf,Final Volcano Plot,
Based on the complete workflow we executed, here is the full, ready-to-copy README.md file for your GitHub repository.

This file provides the necessary context, methodology, and a summary of the analysis steps and results.

DGE Analysis of GSE152641 RNA-Seq Data: Significant Genes via edgeR/Galaxy.

This repository documents and stores the results of a Differential Gene Expression (DGE) analysis comparing gene expression profiles in whole blood from COVID-19 patients versus Healthy Controls.

The analysis was performed entirely using the edgeR statistical package through the Galaxy Main Server (usegalaxy.org) interface.

🔬 Dataset Details

Parameter	Value
GEO Accession	GSE152641
Title	Transcriptomic Similarities and Differences in Host Response between SARS-CoV-2 and Other Viral Infection
Organism	Homo sapiens
Experiment Type	Expression profiling by high throughput sequencing (Bulk RNA-Seq)
Samples Analyzed	86 total samples (62 COVID-19 patients and 24 healthy controls)
Original Publication	Thair SA et al. iScience (2021)

The original study profiled peripheral blood to understand similarities and differences in the host response to SARS-CoV-2 compared to other acute viral infections.

💻 Methodology

The differential expression was determined using the edgeR package on the Galaxy platform, which is optimized for count-based RNA-Seq data.

Workflow:

    Data Input: The pre-processed count matrix (GSE152641_Inflammatix_COVID19_counts_entrez.csv) was uploaded alongside a custom metadata file (GSE152641 Metadata.csv) defining the Group factor.

    Analysis: The edgeR tool was run, specifying the contrast as COVID_19-Control using a single Count Matrix input.

    Filtering: The statistical results were filtered to identify genes meeting the required thresholds:

        Statistical Significance: FDR<0.05 (False Discovery Rate)

        Log Fold Change: ∣logFC∣>0.5 (Used to filter for biologically relevant magnitude)

    Visualization: A final Volcano Plot was generated to summarize the statistically significant gene expression changes.

📈 Key Results and Files

The main outcome of the analysis is the list of genes showing significant changes in the COVID-19 group relative to the Control group.
File Name	Description	Purpose
edgeR_COVID_19-Control.tsv	Primary Results Table. Contains logFC, PValue, and FDR for all ∼20,000 genes.	Used for all subsequent filtering and visualization steps.
Galaxy17-[Scatterplot on dataset 15].pdf	Final Volcano Plot	
Shutterstock

| Visual summary of the differential expression. Genes lying above the horizontal line (FDR<0.05) are significant. | | mdsplot_Group.pdf | MDS Plot (Sample Clustering) | Quality Control check confirming that the 62 COVID-19 samples successfully cluster separately from the 24 Control samples. | | Upregulated_Genes_Fixed.tabular | Final Filtered List. Genes with logFC>0.5 and FDR<0.05. | List of genes upregulated in COVID-19 patients. | | Downregulated_Genes_Fixed.tabular | Final Filtered List. Genes with logFC<−0.5 and FDR<0.05. | List of genes downregulated in COVID-19 patients. |
🚀 Next Steps (Future Analysis)

The final filtered gene lists are ready for functional analysis:

    Gene Annotation: Use tools like BioMart or the NCBI Entrez database to convert the numerical Gene IDs into common gene symbols (e.g., S100A12, IFI27).

    Pathway Enrichment: Submit the lists of upregulated and downregulated genes to a tool like DAVID or GSEA to identify the biological pathways (e.g., "Neutrophil Activation," "Interferon Signaling") that are significantly affected by the infection.

