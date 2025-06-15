# `solveblock` reproducibility

This repo contains code to reproduce the result in our paper [It’s a wrap: deriving distinct discoveries with FDR control after a GWAS pipeline](https://www.biorxiv.org/content/10.1101/2025.06.05.658138v1?rss=1)

:warning: Note these source codes are *purely for review and reproducibility purposes*. Users interested in running the overall pipeline should proceed to the main [GhostKnockoffGWAS](https://github.com/biona001/GhostKnockoffGWAS) page.

## Software versions

All simulations and real data analysis relied on [v0.2.4](https://github.com/biona001/GhostKnockoffGWAS/releases/tag/v0.2.4) of `GhostKnockoffGWAS` and `solveblock`. 

## Running the GhostKnockoff pipeline (for real data and simulated experiments)

This consisted of 3 steps:
1. Running `snp_ldsplit` of `bigsnpr` to obtain quasi-independent regions in each chromosome. Note that in our paper this is considered a pre-processing step. In any case, this was carried out in notebooks `GhostKnockoffGWAS-ldsplit-UKB-array-british.ipynb` and `GhostKnockoffGWAS-ldsplit-UKB-array-otherpop.ipynb`
2. Running `solveblock` executable. This was done in `GhostKnockoffGWAS-solveblock-UKB.ipynb` and `GhostKnockoffGWAS-solveblock-UKB-otherpop.ipynb`
3. Running the `GhostKnockoffGWAS` executable
    + For simulated experiments, see [Simulated Experiments](#Simulated-Experiments)
    + For real data analysis, see [Real data analysis on UKB phenotypes](#Real-data-analysis-on-UKB-phenotypes)

## UK Biobank data quanlity control

This was achieved in `ukb_phenotypes_QC.ipynb` and `ukb_phenotypes_QC_Indians.ipynb`. 

## Simulated Experiments

Check out the following notebooks:
+ `GhostKnockoffGWAS-simulations-UKB.ipynb`: for simulations using (unrelated) British samples
+ `GhostKnockoffGWAS-simulations-UKB-otherpop.ipynb`: for simulations using (related) Indian/Caribbean/Chinese/African samples
+ `GhostKnockoffGWAS-simulations-plots.ipynb`: for code to make **Figure 2** in our paper

## Real data analysis on UKB phenotypes

This was achieved in `GhostKnockoffGWAS-UKB-26-phenotypes.ipynb`.

## Questions?

Please raise an issue on this repo, or you can directly email Benjamin Chu <benchu99@Hotmail.com> and Chiara Sabatti <sabatti@stanford.edu>
