# TCGA-capture-RNASeq-analysis
This project examines differences in gene expression levels between polyA and capture methods applied to cancer tissues

Main scripts:
expression_analysis-Github.ipynb (analyze differences between polyA and capture of every gene and add correction factors) 
gencode_analysis-Github.ipynb (find differences in gene records between gencode and capture)

Main input files:

truseq-rna-exome-targeted-regions-manifest-v1-2.bed (on Illumina) -> liftover to V38

gencode.v22.annotation.gtf (on GENCODE)

complete_genome_data.txt (final consensus on the amount/percents of gene transcripts captured)

ABSTRACT
RNA-Seq is a useful tool for understanding gene expression. Transcriptome data provides information about genes such as expression levels, splicing patterns, and mutation expression.  With this information we can identify genes that significantly vary in expression level in cancer cells compared to similar cells from normal tissue. We are studying the RNA-Seq profiles of 113 cancer patients, who lived much longer than expected, given the advanced stage and treatment they received.  They are referred to as exceptional responders (ER) and our goal is to determine the genetic features that contributed to extend the lives of those patients. To identify those key genes, we compare gene expression data from the ER patients to that of 33 common cancers reported from The Cancer Genomics Atlas (TCGA) project. Our ER patient’s tissues were formalin-fixed paraffin-Embedded (FFPE) to preserve their histology. However, FFPE severely degrades RNA fragments, whereas tissues from TCGA were prepared from fresh frozen (FF) in liquid nitrogen. This required us to use a different methodology for generating RNA Seq sequencing libraries called “exome capture” as opposed to the method used in TCGA known as “polyA selection”.  The capture arrays enable us to sequence only exons of a transcript that are targeted by the capture exome array, whereas polyA enrichment can sequence any RNA with a polyA tail in its full length. We have discovered that these two different library preparation approaches lead to different results using RNA from the same tissue. About 1/3 of all genes yield widely differing results. We need to find out why the methods differ and develop methods to correct for the differences.  One explanation for the differences we see could be due to differences in how the transcripts are structured by the exome capture array and the known full-length transcripts.  My project has involved detailed comparison of the exome capture target exons to the exon tables from full length transcripts detailed by GenCode, a database of reference gene transcripts. 
Using Python and R programming for processing data, I demonstrated that 8,039 out of the 19,712 protein-coding genes have 90-100% of their exons known to GenCode represented on the capture array.  However, for another 1,975 genes, I could identify less than 30% of their exons known to GenCode are targeted in the capture array. May last step is to correlate the genes with less than 30% of exons targeted to the list of genes with variable expression levels.  This is ongoing.  This correlation would give us hints on variable gene expression levels between the two library preparation methods. Finally, these results will shed light on the understanding of patients’ tumor profiles so that we will more accurately discover specific gene candidates for cancer treatment target. 
