# Memis-Bilgici-R-Assignment
 Memis Bilgici R assignment is consist of three parts:
1. Replicating my UNIX assignment in R
2. Additional analysis and visualization
3. Reviewing two assignments from my peers (aksharar@iastate.edu and chram@iastate.edu)
Memis Bilgici R Assignment Overview
This R Assignment is to process and analyze SNP genotype data from maize and teosinte. The analysis replicates a previous UNIX-based SNP processing workflow using R. 
The main aim is to:
PART 1 (Data Inspection) and PART 2 (Visulation) 
- Load and clean SNP data
- Handle non-numeric chromosome values
- Generate formatted output files for further analysis
- Visualize SNP distributions and genotype proportions
- Ensure correct processing for publication-quality results
Data Processing Pipeline
Step 1: Load and Filter Genotype Data
The raw genotype file (fang_et_al_genotypes.txt) is loaded.
Samples are split into Maize and Teosinte groups.
Step 2: Handle Non-Numeric Chromosomes
Non-numeric chromosome values ("multiple", "unknown") are logged and excluded from analysis.
Step 3: Format and Sort SNP Data
SNPs are sorted increasingly and decreasingly per chromosome.
Files are generated separately for maize and teosinte.
Step 4: Generate Visualizations
SNP Distribution per Chromosome
SNP_Distribution.png
Histogram of SNP Positions
SNP_Position_Histogram.png
Proportion of Homozygous, Heterozygous, and Missing Data
Genotype_Proportions.png
Output
File Name	Description
maize_chr*_inc.txt	SNPs sorted in increasing order (per chromosome)
maize_chr*_dec.txt	SNPs sorted in decreasing order (per chromosome)
teosinte_chr*_inc.txt	SNPs sorted in increasing order (per chromosome)
teosinte_chr*_dec.txt	SNPs sorted in decreasing order (per chromosome)
SNP_Distribution.png	Bar plot of SNP count per chromosome
SNP_Position_Histogram.png	Histogram of SNP positions along chromosomes
Genotype_Proportions.png	Stacked bar plot of genotype proportions
Part I
Data Inspection
1. fang_et_al_genotypes.txt : a published SNP data set including maize, teosinte
(i.e., wild maize), and Tripsacum (a close outgroup to the genus Zea) individuals.
2. snp_position.txt : an additional data file that includes the SNP id (first column),
chromosome location (third column), nucleotide location (fourth column) and other
information for the SNPs genotyped in the fang_et_al_genotypes.txt file.
Data Processing
fang_et_al_genotypes.txt # Raw genotype data │ snp_position.txt # SNP position data │  Non_Numeric_Chromosomes.tsv # Non-numeric chromosome SNPs (logged) │ Non_Numeric_Chromosomes_Teosinte.tsv # Non-numeric chromosome SNPs for teosinte │
output/ 
maize_chr_inc.txt # SNPs sorted in increasing order (per chromosome)
maize_chr_dec.txt # SNPs sorted in decreasing order (per chromosome) 
teosinte_chr_inc.txt # SNPs sorted in increasing order (per chromosome)
teosinte_chr_dec.txt # SNPs sorted in decreasing order (per chromosome) 
SNP_Distribution.png # SNP distribution across chromosomes
SNP_Position_Histogram.png # Histogram of SNP positions
Genotype_Proportions.png # Proportion of homozygous, heterozygous, and missing data
SNP_Analysis.R # Main R script for data processing and visualization 
README.md R Assignment documentation

