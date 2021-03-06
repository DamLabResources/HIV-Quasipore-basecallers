# HIV-Quasipore-basecallers

HIV-Quasipore is an HIV-1-specific Nanopore basecaller suite designed to substantially improve HIV-1 read quality and enhance viral quasispecies (vQs) detection. It comes in three versions: fast, high-accuracy (HAC) and super-accuracy (SUP) for R9.4.1 basecalling and HAC and SUP for R10.3 basecalling. 

The fast basecaller is designed for live basecalling, while HAC and SUP basecallers are designed for pipeline incorperation. While their primary purpose is to enhance HIV vQs detection, it can be applied for other HIV-1-specific applications, including but not limited to:

* HIV-1 CRISPR-induced InDel detection
* Whole genome amplification
* Integration site studies
* vQs-specific *tat* and *rev* exon matching
* Coevolution studies

## Citation
```
@ARTICLE
{10.3389/fviro.2022.858375,  
author{Link, Robert W. and De Souza, Diehl R. and Spector, Cassandra and Mele, Anthony R. and Chung, Cheng-Han and Nonnemacher, Michael R. and Wigdahl, Brian and Dampier, Will},   	 
journal={Frontiers in Virology},      	
title={HIV-Quasipore: A Suite of HIV-1-Specific Nanopore Basecallers Designed to Enhance Viral Quasispecies Detection}, 
year={2022},    
volume={2},
url={https://www.frontiersin.org/article/10.3389/fviro.2022.858375},       	
doi={10.3389/fviro.2022.858375}}
```
## Basecallers

|Basecaller|File|
|--|--|
|R9.4.1 HIV-Quasipore (fast) | fast_r941_final.json |
|R9.4.1 HIV-Quasipore (high accuracy) | hac_r941_final.json |
|R9.4.1 HIV-Quasipore (super accuracy) | sup_r941_final.json |
|R10.3 HIV-Quasipore (high accuracy) | hac_r103_final.json |
|R10.3 HIV-Quasipore (super accuracy) | sup_r103_final.json |

## Use template

```bash
# R9.4.1 HIV-Quasipore-HAC example
$ guppy_basecaller -s <outdir> -i <read_dir> -x cuda:0 -m hac_r941_final.json
```


