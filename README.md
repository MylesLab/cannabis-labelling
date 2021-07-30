# Cannabis project

This repository contains the code and data for the analysis of Cannabis samples for the manuscript titled "Cannabis labelling is associated with genetic variation in terpene synthase genes". This project involved the analysis of terpene and cannabinoid data from a previously published paper (Hazekamp et al. 2016) and a newly generated SNP dataset from Cannabis samples collected across the Netherlands.

The genetic data used in the genetic analysis can be found on DRYAD:

* 20191209\_bedrocan\_gen_filtered.map
* 20191209\_bedrocan\_gen_filtered.ped
* 20191209\_bedrocan\_gen_filtered.nosex
* 20191209\_bedrocan\_gen\_filtered_pruned.raw
* 20191209\_bedrocan\_gen_filtered.mdist
* 20191209\_bedrocan\_gen_filtered.mdist.id
* 20191209\_bedrocan\_gen_filtered.genome
* 20191209\_bedrocan\_gen_filtered.hmp.txt
* 202008011\_bedrocan\_gen_filtered.raw
* 2020080607\_bedro_kinship.txt


**Please note that the genetic data files generated in this study have chromosomes numbered based on the old numbering system. Within the 'cannabis GWAS' source code the chromosomes are renumbered for presentation in the Manhattan plots according to the new chromosome numbering system for the CBDRx reference genome that was adopted in 2020 (<https://www.ncbi.nlm.nih.gov/assembly/GCF_900626175.2>). All resulting figures from the GWAS follow the new numbering system, however, the raw genetic files still reflect the old numbering system and should be recoded if used by others in the future.**

**During the review process some chemical names from the Hazekamp et al. 2016 paper were renamed, these changes are recorded in Supplementary Table 3 and described within the methods of the manuscript.**

## Data

**170428 Bedrocan\_chem_sample mg per g.xlsx** Raw chemical data file that contains terpenes and cannabinoid concentrations across 297 samples.

**short\_chem_names.txt** Table with the short hand names for the chemical compounds.

**sesqui_genes.xlsx** Excel file containing annotations and bp positions for genes within the regions of interest on chromosome 6.

**mono_genes.xlsx** Excel file containing annotations and bp positions for genes within the regions of interest on chromosome 5.


## Source

**cannabis\_data_cleanup.Rmd:** code used to clean up the chemical data.

**cannabis_analysis.Rmd:** code used to do the analyses for PCA and chemical correlations with label types.

**cannabis_supplements.Rmd** code used to do the supplemental analyses.

**cannabis\_simple_m.Rmd** code to calculate the effective number fo independant tests for multiple test correction of the GWAS results.

**cannabis_gwas.Rmd** code for running the standard (EMMAX) and multi-locus mixed model (MLMM) gwas.

**cannabis\_zoom_ld.Rmd** code for creating zoom in figures of GWAS resutls with LD heatmaps.


## Outputs

**chem\_data.csv** Full chemical data for 297 samples that has been cleaned up.

**gen\_chem_data.csv** Chemical data for 137 samples that also have genetic data.

**pc\_chem_load.R** Chemical PC loadings 1-10 from 297 samples along with Sativa-indica labels.

**pc\_geno_load.R** Genetic PC loadings 1-10 from 137 samples along with Sativa-indica labels.

**chem\_lm_tab.txt** output statistics from the correlation label type with chemical concentration.

**heatmap_pvals.csv** P-values from Pearson correlations between chemical concentrations.

**heatmap_r.csv** Estimates (r) from Pearson correlations between chemical concentrations.

**gwas\_pvals_emmax.csv** P-values from the standard emmax gwas with un-normalized chemical data.

**gwas\_pvals_mlmm.csv** P-values from the MLMM gwas with un-normalized chemical data.

**snp\_r2** a sub directory that contains the outputs for the variance explained by the top SNPs included as co-factors in the mlmm GWAS with the un-normalized chemical data.

**gwas\_pvals\_emmax_norm.csv** P-values from the standard emmax gwas with normalized chemical data.

**gwas\_pvals\_mlmm_norm.csv** P-values from the MLMM gwas with normalized chemical data.

**snp\_r2_norm** a sub directory that contains the outputs for the variance explained by the top SNPs included as co-factors in the mlmm GWAS with the normalized chemical data.


## Figures

This directory contains the figures created in from the scripts above.

**gwas** is a sub directory that contains:

* **mlmm\_results** a pdf with MLM and MLMM GWAS plots that used un-normalized chemical data.
* **mlmm\_results_norm** a pdf with MLM and MLMM GWAS plots that used normalized chemical data.

## Main Figures

This directory contains the final main figures presented in the manuscript.

## Supplementary files

This directory contains the supplementary figures and files.