
# Genome-Scale Perturb-seq Replication
A concise replication of the Cell paper **"Mapping information-rich genotype-phenotype landscapes with genome-scale Perturb-seq"** (2022, DOI: 10.1016/j.cell.2022.05.013).


## Project Overview
Replicated the core workflow of genome-scale Perturb-seq analysis, combining CRISPRi-mediated gene perturbation and single-cell RNA-seq to construct genotype-phenotype maps. Validated key findings of the original study and uncovered novel gene regulatory relationships.


## Data Source
All datasets are from the original study's official repository:  
[https://gwps.wi.mit.edu/](https://gwps.wi.mit.edu/)

Key datasets:
- `K562_essential_normalized_bulk_01.h5ad`: K562 cell line (essential genes perturbation)
- `K562_gwps_normalized_bulk_01.h5ad`: K562 cell line (whole-genome perturbation)
- `Rpe1_normalized_bulk_01.h5ad`: RPE1 cell line (essential genes perturbation)


## Core Replication Content
Successfully reproduced 8 key analytical modules of the original paper:
1. Quality control & strong perturbation screening
2. Gene function annotation via Perturb-seq
3. Cross-dataset perturbation similarity comparison
4. Functional annotation of uncharacterized genes
5. Discovery of novel Integrator complex subunits
6. Genotype-phenotype map construction
7. Transcriptional program & differentiation phenotype analysis
8. Stress-specific regulation of mitochondrial genome

For detailed methods and results, refer to the full **report** document.


## Environment Setup
### Dependencies
```bash
python>=3.8
scanpy, anndata, pymde, hdbscan
scipy, numpy, pandas, seaborn, matplotlib
infercnvpy, pygenometracks
```

### Installation
```bash
pip install -r requirements.txt
```


## Usage
1. Download datasets and place them in the `data/` directory
2. Run core replication: `python main_replication.py`
3. Module-specific scripts are in the `scripts/` folder
4. Results are saved in the `results/` directory


## Novel Discovery
Identified a new regulatory mechanism:  
Exosome complex subunits (DIS3, EXOSC2-8) mediate coordinated degradation of histone genes and dysregulated lncRNA/antisense transcripts. Knockdown of these subunits synchronously upregulates both RNA types, potentially via epigenetic positive feedback.


## Summary
This project verifies the reliability of the original Perturb-seq analytical pipeline. For detailed experimental design, statistical methods, and result interpretations, please refer to the full **report** document.


## References
- Replogle et al. (2022). Mapping information-rich genotype-phenotype landscapes with genome-scale Perturb-seq. *Cell*, 185(14), 2559–2575.
- Full replication details: See attached **report** document.
