# fix-sex-chr.smk, wiki: https://eichlerlab.gs.washington.edu/help/wiki/doku.php?id=users:lettucerap:sex_chromosome_grouping
## Step 1. Prepare directory
```
config
├── config.yaml
└── manifest.tab
runsnake
```
## Step 2. Prepare inputs
### config/config.yaml
```
reference: /net/eichler/vol26/eee_shared/assemblies/CHM13/T2T/v2.0/T2T-CHM13v2.fasta

# OPTIONAL ARGS
minimap_params: '-x asm20 --secondary=no -s 25000'
manifest: config/manifest.tab
```
### config/manifest.tab
```bash
sample  hap1    hap2
your_sample path/to/hap1_asm    /path/to/hap2_asm
```
## Step 3. Start the analysis!
```bash
ln -s /net/eichler/vol27/projects/autism_genome_assembly/nobackups/scratch/wumei/fix_sex_chr/runsnake .
./runsnake 30
```

