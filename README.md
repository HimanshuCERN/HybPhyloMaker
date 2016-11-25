# HybPhyloMaker
   
Set of bash scripts for analysis of HybSeq raw data. Consists of several steps:   
  
0. Download FASTQ files from Illumina BaseSpace storage  
1. Processing raw reads (PhiX removal, adaptor removal, quality filtering, summary statistics)  
2. Mapping reads to reference (using Bowtie), create consensus sequence  
2. Recognize sequences matching probes (generate PSLX files using BLAT)  
3. Create alignments for all genes  
4. Treat missing data, select best genes  
5. Generate FastTree or RAxML gene trees + trees-alignment properties  
6. Root gene trees with outgroup, combine gene trees into a single file  
7. Estimate species tree (ASTRAL, ASTRID, MRL, concatenation)  
8. Subselect suitable genes and repeat steps 6+7 
  
Uses many additional software that must be installed and put in the PATH prior to run scripts (see Table located in docs folder and consider to run install_software.sh).  
Also utilizes many scripts developed by others (located in HybSeqSource folder). PLEASE CITE APPROPRIATELY THOSE SCRIPTS WHEN USING HybPhyloMaker!  

Read manual located in docs folder before running HybPhyloMaker.  

