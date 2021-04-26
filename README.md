# HIV-Quasipore-basecallers

HIV-Quasipore is an HIV-1-specific Nanopore basecaller designed to substantially improve HIV-1 read quality and enhance viral quasispecies (vQs) detection. It comes in two version: fast and high-accuracy (HAC). The former is designed for live basecalling, and the latter deisgned for pipeline incorperation. While its primary purpose is to enhance HIV-vQs detection, it can be applied for other HIV-1-specific applications, including but not limited to:

* HIV-1 CRISPR-induced InDel detection
* Whole genome amplification
* Integration site studies
* vQs-specific *tat* and *rev* exon matching
* Co-evolution studies

## Improvement metrics 
Add pretty figures later

## Use template

```bash
# Undo tarball to use basecaller
$ tar -xf HIV-Quasipore-<type>.json.tar.gz

# HIV-Quasipore-HAC example
$ guppy_basecaller -s <outdir> -i <read_dir> -r -c dna_r9.4.1_450bps_hac.cfg -x cuda:0 --qscore_offset -6.98 --qscore_scale 2.92 -m HIV-Quasipore-high-accuracy.json

# HIV-Quasipore-fast example
$ guppy_basecaller -s <outdir> -i <read_dir> -r -c dna_r9.4.1_450bps_fast.cfg -x cuda:0 --qscore_offset -18.67 --qscore_scale 4.0 -m HIV-Quasipore-fast.json
```

## Citation
TBD
