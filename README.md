# HybPhyloMaker
   
> Fér T. & Schmickl R. (2018): [HybPhyloMaker: target enrichment data analysis from raw reads to species trees.](http://journals.sagepub.com/doi/10.1177/1176934317742613) *Evolutionary Bioinformatics* 14: 1-9. doi: 10.1177/1176934317742613  
   
**Set of bash scripts for analysis of HybSeq data (from raw reads to species trees).** Consists of several steps:   
  

0:  Prepare FASTQ files to folder (optionally download files from Illumina BaseSpace storage)  
1:  Processing raw reads (PhiX removal, adaptor removal, quality filtering, summary statistics)  
2:  Mapping reads to reference (using Bowtie2/BWA), create consensus sequence  
3:  Recognize sequences matching probes (generate PSLX files using BLAT)  
4:  Create alignments for all genes (+ optionally correct reading frame and/or select low heterozygosity loci)  
5:  Treat missing data, select best genes  
6:  Generate FastTree or RAxML gene trees + calculate/plot trees-alignment properties  
7:  Root gene trees with outgroup, combine gene trees into a single file  
8:  Estimate species tree (ASTRAL, ASTRID, MRL, BUCKy, concatenation)  
9:  Subselect suitable genes and repeat steps 7+8  
10:Subselect trees based on samples presence, collapse unsupported branches  
  
Uses many additional software that must be installed and put in the PATH prior to run scripts (see [Table](docs/HybPhyloMaker_software.pdf) located in docs folder and consider to run [install_software.sh](install_software.sh)).  
Also utilizes many scripts developed by others (located in [HybSeqSource folder](HybSeqSource)). PLEASE CITE APPROPRIATELY THOSE SCRIPTS WHEN USING HybPhyloMaker!  

Read [manual](docs/HybPhyloMaker_manual1.6.4.pdf) located in docs folder before running HybPhyloMaker.  

# HybPhyloMaker workflow
![HybPhyloMaker workflow](https://github.com/tomas-fer/HybPhyloMaker/blob/master/docs/HybPhyloMaker_workflow.png)

# Papers citing HybPhyloMaker
Carlsen MM, Fér T, Schmickl R, Leong-Škorničková J, Newman M, Kress WJ. 2018. [Resolving the rapid plant radiation of early diverging lineages in the tropical Zingiberales: Pushing the limits of genomic data](https://www.sciencedirect.com/science/article/pii/S1055790317309296). Molecular Phylogenetics and Evolution 128:55-68. doi: 10.1016/j.ympev.2018.07.020  
Herrando-Moraira S, Cardueae Radiations Group. 2018. [Exploring data processing strategies in NGS target enrichment to disentangle radiations in the tribe Cardueae (Compositae)](https://www.sciencedirect.com/science/article/pii/S1055790318302501). Molecular Phylogenetics and Evolution 128:69-87. doi: 10.1016/j.ympev.2018.07.012  
Villaverde T, Pokorny L, Olsson S, Rincón-Barrado M, Johnson MG, Gardner EM, Wickett NJ, Molero J, Riina R, Sanmartín I. 2018. [Bridging the micro- and macroevolutionary levels in phylogenomics: Hyb-Seq solves relationships from populations to species and above](https://nph.onlinelibrary.wiley.com/doi/abs/10.1111/nph.15312). New Phytologist. doi: 10.1111/nph.15312
